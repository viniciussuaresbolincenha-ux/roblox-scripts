// script.js – módulo ES6
type Product = {
    id: number;
    title: string;
    price: number;
    image: string;
};

type CartItem = {
    product: Product;
    quantity: number;
};

class Store {
    private products: Product[] = [];
    private cart: Map<number, CartItem> = new Map();

    constructor() {
        this.init();
    }

    /** Carrega produtos simulando chamada a API */
    private async loadProducts(): Promise<void> {
        try {
            // Simulação de fetch; substitua por endpoint real se necessário
            const response = await fetch('https://fakestoreapi.com/products?limit=8');
            if (!response.ok) throw new Error('Falha ao buscar produtos');
            const data = await response.json();

            // Normaliza para nosso modelo
            this.products = data.map((p: any) => ({
                id: p.id,
                title: p.title,
                price: Number(p.price),
                image: p.image
            }));
        } catch (err) {
            console.error('Erro ao carregar produtos:', err);
            // Fallback com dados estáticos
            this.products = [
                {
                    id: 1,
                    title: 'Smartphone XYZ',
                    price: 1499.99,
                    image: 'https://via.placeholder.com/300x180?text=Smartphone'
                },
                {
                    id: 2,
                    title: 'Fone Bluetooth ABC',
                    price: 299.90,
                    image: 'https://via.placeholder.com/300x180?text=Fone+Bluetooth'
                },
                // ... adicione mais itens conforme desejar
            ];
        }
    }

    /** Renderiza a grade de produtos */
    private renderProducts(): void {
        const grid = document.getElementById('productGrid');
        if (!grid) return;

        grid.innerHTML = '';
        this.products.forEach(p => {
            const card = document.createElement('article');
            card.className = 'product-card';
            card.innerHTML = `
                <img src="${p.image}" alt="${p.title}" class="product-image" loading="lazy">
                <div class="product-info">
                    <h3 class="product-title">${p.title}</h3>
                    <p class="product-price">R$ ${p.price.toFixed(2).replace('.', ',')}</p>
                    <button class="add-to-cart" data-id="${p.id}">Adicionar ao carrinho</button>
                </div>
            `;
            grid.appendChild(card);
        });

        // Delegação de eventos para botões "Adicionar"
        grid.addEventListener('click', (e) => {
            const target = e.target as HTMLElement;
            if (target.matches('.add-to-cart')) {
                const id = Number(target.dataset.id);
                this.addToCart(id);
            }
        });
    }

    /** Adiciona produto ao carrinho */
    private addToCart(productId: number): void {
        const product = this.products.find(p => p.id === productId);
        if (!product) return;

        const existing = this.cart.get(productId);
        if (existing) {
            existing.quantity += 1;
        } else {
            this.cart.set(productId, { product, quantity: 1 });
        }
        this.updateCartBadge();
    }

    /** Atualiza contagem no ícone do carrinho */
    private updateCartBadge(): void {
        const countEl = document.getElementById('cartCount');
        if (!countEl) return;
        const totalQty = Array.from(this.cart.values())
            .reduce((sum, item) => sum + item.quantity, 0);
        countEl.textContent = String(totalQty);
    }

    /** Abre o dialog do carrinho */
    private openCart(): void {
        const dialog = document.getElementById('cartDialog') as HTMLDialogElement;
        if (!dialog) return;

        const list = document.getElementById('cartItems');
        const totalEl = document.getElementById('cartTotal');
        if (!list || !totalEl) return;

        list.innerHTML = '';
        let total = 0;

        this.cart.forEach(({ product, quantity }) => {
            const li = document.createElement('li');
            li.className = 'cart-item';
            li.innerHTML = `
                <span>${product.title} (x${quantity})</span>
                <span>R$ ${(product.price * quantity).toFixed(2).replace('.', ',')}</span>
            `;
            list.appendChild(li);
            total += product.price * quantity;
        });

        totalEl.textContent = total.toFixed(2).replace('.', ',');
        dialog.showModal();
    }

    /** Finaliza compra (simulação) */
    private async checkout(): Promise<void> {
        if (this.cart.size === 0) {
            alert('Seu carrinho está vazio.');
            return;
        }
        try {
            // Simular chamada de checkout
            await new Promise(res => setTimeout(res, 1000));
            alert('Compra concluída com sucesso!');
            this.cart.clear();
            this.updateCartBadge();
            const dialog = document.getElementById('cartDialog') as HTMLDialogElement;
            dialog?.close();
        } catch (err) {
            console.error('Erro no checkout:', err);
            alert('Ocorreu um erro ao processar a compra.');
        }
    }

    /** Configura listeners globais */
    private bindUI(): void {
        const cartBtn = document.getElementById('cartBtn');
        const closeBtn = document.getElementById('closeCartBtn');
        const checkoutBtn = document.getElementById('checkoutBtn');

        cartBtn?.addEventListener('click', () => this.openCart());
        closeBtn?.addEventListener('click', () => {
            const dlg = document.getElementById('cartDialog') as HTMLDialogElement;
            dlg?.close();
        });
        checkoutBtn?.addEventListener('click', () => this.checkout());
    }

    /** Inicializa a aplicação */
    private async init(): Promise<void> {
        await this.loadProducts();
        this.renderProducts();
        this.bindUI();
    }
}

// Instancia a loja ao carregar a página
window.addEventListener('DOMContentLoaded', () => new Store());
