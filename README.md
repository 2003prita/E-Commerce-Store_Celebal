# E-Commerce-Store_Celebal
import React from 'react';
import ProductItem from './ProductItem';

const ProductList = ({ products }) => {
  return (
    <div className="product-list">
      {products.map(product => (
        <ProductItem key={product.id} product={product} />
      ))}
    </div>
  );
};

export default ProductList;
import React from 'react';

const ProductItem = ({ product }) => {
  return (
    <div className="product-item">
      <h3>{product.name}</h3>
      <p>{product.description}</p>
      <p>Price: ${product.price}</p>
      {/* Add to cart button */}
      <button>Add to Cart</button>
    </div>
  );
};

export default ProductItem;
import React from 'react';

const Cart = ({ cartItems }) => {
  return (
    <div className="cart">
      <h2>Shopping Cart</h2>
      <ul>
        {cartItems.map(item => (
          <li key={item.id}>
            {item.name} - Quantity: {item.quantity}
          </li>
        ))}
      </ul>
      {/* Checkout button */}
      <button>Proceed to Checkout</button>
    </div>
  );
};

export default Cart;
import React from 'react';

const Checkout = () => {
  return (
    <div className="checkout">
      <h2>Checkout</h2>
      {/* Form for shipping address, payment details, etc. */}
      <form>
        {/* Form fields */}
        <input type="text" placeholder="Name" />
        <input type="email" placeholder="Email" />
        {/* Other fields */}
        <button>Place Order</button>
      </form>
    </div>
  );
};

export default Checkout;
