VALIDAÇÃO

import React, { useState } from 'react';
import { Button, Form } from 'react-bootstrap';

const Formulario = () => {
  const [name, setName] = useState('');
  const [price, setPrice] = useState('');
  const [image, setImage] = useState('');
  const [validated, setValidated] = useState(false);

  const handleSubmit = (event) => {
    const form = event.currentTarget;
    if (form.checkValidity() === false) {
      event.preventDefault();
      event.stopPropagation();
    }

    setValidated(true);
  };

  return (
    <Form noValidate validated={validated} onSubmit={handleSubmit}>
      <Form.Group controlId="formProductName">
        <Form.Label>Nome do Produto</Form.Label>
        <Form.Control
          required
          type="text"
          placeholder="Digite o nome do produto"
          value={name}
          onChange={(e) => setName(e.target.value)}
        />
        <Form.Control.Feedback type="invalid">
          Por favor, digite o nome do produto.
        </Form.Control.Feedback>
      </Form.Group>

      <Form.Group controlId="formProductPrice">
        <Form.Label>Preço do Produto</Form.Label>
        <Form.Control
          required
          type="number"
          placeholder="Digite o preço do produto"
          value={price}
          onChange={(e) => setPrice(e.target.value)}
        />
        <Form.Control.Feedback type="invalid">
          Por favor, digite o preço do produto.
        </Form.Control.Feedback>
      </Form.Group>

      <Form.Group controlId="formProductImage">
        <Form.Label>Imagem do Produto</Form.Label>
        <Form.Control
          required
          type="text"
          placeholder="Digite o URL da imagem do produto"
          value={image}
          onChange={(e) => setImage(e.target.value)}
        />
        <Form.Control.Feedback type="invalid">
          Por favor, digite o URL da imagem do produto.
        </Form.Control.Feedback>
      </Form.Group>

      <Button type="submit">Cadastrar Produto</Button>
    </Form>
  );
};

export default ;
