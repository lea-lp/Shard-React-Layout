# Shards React Layout

Documentation : https://designrevision.com/docs/shards-react/getting-started

## Installation

```bash

$yarn add shards-react

```

## Imports

```js
// EntryPoint > src/index.js
import "bootstrap/dist/css/bootstrap.min.css";
import "shards-ui/dist/css/shards.min.css"

// In components
import { Alert } from "shards-react";
```

## Synthax

> Shards is a Bootstrap template.

```js
// Colors
<Element theme="primary">Primary</Element>

```

```js
// Size
<Element size="sm">Small</Element>
```

```js
// Margin, Padding
<Element className="ml-5 pt-auto">Card</Element>
```

```js
// Style
<Element style={{ maxWidth: "300px" }}>Primary</Element>
```

## Components examples

### Alerts

```js
​      <Alert theme="primary">
​        Alert - Primary Theme (default) -{" "}
​        <a className="alert-link" href="#">
​          Example Link
​        </a>
​      </Alert>
```

### Card

```js
​    <Card style={{ maxWidth: "300px" }}>
​      <CardHeader>Card header</CardHeader>
​      <CardImg src="https://place-hold.it/300x200" />
​      <CardBody>
​        <CardTitle>Lorem Ipsum</CardTitle>
        <p>Lorem ipsum dolor sit amet.</p>
​        <Button>Read more &rarr;</Button>
​      </CardBody>
​      <CardFooter>Card footer</CardFooter>
​    </Card>
```

### Grid

```js
  <Container>
​    <Row>
​      <Col>Col 1</Col>
​      // Responsive
​      <Col sm="12" md="4" lg="3">Col 2</Col>
​      // Responsive custom styling
​      <Col sm={{ size: 8, order: 2, offset: 2 }}>Col 3</Col>
​    </Row>
  </Container>
```

### Modal

```js
 constructor(props) {
​    super(props);
​    this.state = { open: false };
​    this.toggle = this.toggle.bind(this);
  }

  toggle() {
​    this.setState({
​      open: !this.state.open
​    });
  }

  render() {
​    const { open } = this.state;

​    return (
      <div>
​        <Button onClick={this.toggle}>Click Me!</Button>
​        <Modal open={open} toggle={this.toggle}>
​          <ModalHeader>Header</ModalHeader>
​          <ModalBody>👋 Hello there!</ModalBody>
​        </Modal>
​      </div>
​    );
  }
```
