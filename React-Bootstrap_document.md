# React-BootStrap 설치 및 사용법

## React-BootStrap이란?

부트스트랩(Bootstrap)은 오픈소스 프론트엔드 프레임워크로, 웹사이트를 쉽게 만들 수 있도록 각종 레이아웃, 버튼, 입력창 등의 디자인을 CSS 및 JavaScript로 만들어 제공한다. React에서는 이와 같은 부트스트랩을 React-Bootstrap을 통해 사용할 수 있다.
React-Bootstrap은 기존의 부트스트랩을 React 스타일의 컴포넌트로 압축하여 간결한 코드로 구현할 수 있도록 도와준다.

## 설치 방법

React-Bootstrap의 npm으로 설치할 수 있는 npm 패키지를 사용할 수 있다. (원하는 경우 yarn으로 설치할 수 있다.)

- npm을 통한 React-Bootstrap 패키지 설치

```bash
npm install react-bootstrap bootstrap
```

- yarn을 통한 React-Bootstrap 패키지 설치

```bash
yarn add react-bootstrap bootstrap
```

yarn 또는 npm 으로 설치 시 src/index.js에 `import 'bootstrap/dist/css/bootstrap.css';` 를 추가해야 한다.

## 컴포넌트 import하기

다음과 같이 개별 컴포넌트 요소를 가져올 수 있으며, 이는 사용할 특정 컴포넌트 요소만 가져오므로 client에 보내는 코드의 양을 감소시킬 수 있다.

```javascript
import {컴포넌트 태그명, ...} from 'react-bootstrap';
```

예) Button 컴포넌트를 사용하려는 경우
```javascript
import { Button } from 'react-bootstrap';
//또는
import Button from 'react-bootstrap/Button';
```

## 컴포넌트 종류

- [Buttons](#buttons)
- [Cards](#cards)
- [Carousels](#carousels)
- [Dropdowns](#dropdowns)
- [Forms](#forms)
- [InputGroup](#inputgroup)
- [List groups](#list-groups)
- [Modals](#modals)
- [Navbars](#navbars)
- [Offcanvas](#offcanvas)
- [Progress bars](#progress-bars)
- [Spinners](#spinners)
- [Tables](#tables)
- [Tabs](#tabs)

## 컴포넌트 사용 방법

## Buttons

### Basic buttons

variant 속성 변경만으로 스타일이 지정된 버튼을 빠르게 생성할 수 있다.

- **코드**
```javascript
import { Button } from 'react-bootstrap';

<>
  <Button variant="primary">Primary</Button>
  <Button variant="secondary">Secondary</Button>
  <Button variant="success">Success</Button>
  <Button variant="warning">Warning</Button>
  <Button variant="danger">Danger</Button> 
  <Button variant="info">Info</Button>
  <Button variant="light">Light</Button> 
  <Button variant="dark">Dark</Button>
  <Button variant="link">Link</Button>
</>
```
- **적용 모습**

<img src="https://user-images.githubusercontent.com/55876471/147387721-88bfe78e-007f-4e7f-969a-307069efcc22.png" width="750" height="70"/>

### Outline buttons
variant 속성에 `outline-*`을 적용하여 배경색이 없는 버튼을 생성할 수 있다.

- **코드**

```javascript
import { Button } from 'react-bootstrap';

<>
  <Button variant="outline-primary">Primary</Button>
  <Button variant="outline-secondary">Secondary</Button>
  <Button variant="outline-success">Success</Button>
  <Button variant="outline-warning">Warning</Button>
  <Button variant="outline-danger">Danger</Button>
  <Button variant="outline-info">Info</Button>
  <Button variant="outline-light">Light</Button>
  <Button variant="outline-dark">Dark</Button>
</>
```
- **적용 모습**
  - **기본**
  <img src="https://user-images.githubusercontent.com/55876471/147388557-19f372dd-3a67-4614-9964-0d30b9d6393b.png" width="790" height="70"/>

  - **마우스 hover 시**

    variant 속성에 `outline-*`을 적용한 버튼의 경우, 마우스 hover 시 다음과 같이 배경색이 채워진다.
  <img src="https://user-images.githubusercontent.com/55876471/147388430-95d22bde-8abc-4049-8253-1a3cce9ed469.gif" width="800" height="110"/>


### Button groups
Button group 태그를 통해 여러 개의 버튼을 하나의 라인으로 그룹화할 수 있다. 이때 aria-label 속성을 이용하여 버튼 그룹을 설명할 수 있다.

- **코드**

```javascript
import { ButtonGroup, Button } from 'react-bootstrap';

<>
  <ButtonGroup aria-label="Button group">
    <Button variant="primary">button1</Button>
    <Button variant="primary">button2</Button>
    <Button variant="primary">button3</Button>
  </ButtonGroup>
</>
```
- **적용 모습**

<img src="https://user-images.githubusercontent.com/55876471/147388813-29bffb33-04d4-4050-964c-fe481a8f7c2e.png" width="700" height="90"/>

-----
## Cards
Card 컴포넌트를 여러 옵션과 함께 사용하여 유연하고 확장 가능한 content container를 만들 수 있다.

- **Card 컴포넌트 요소**
  - `<Card>`
  - `<Card.Header>`
  - `<Card.Title>`
  - `Card.Subtitle`
  - `<Card.Body>`
  - `<Card.Text>`
  - `<Card.Img>`
  - `<Card.ImgOverlay>`
  - `<Card.Link>`
  - `<Card.Footer>`
  - `<CardGroup>`

위의 요소들을 이용하여 Card 내부에 헤더, 제목, 부제목, 내용, 이미지/링크 삽입, 그룹화 등이 가능하다.

- **코드**

```javascript
import { Card } from 'react-bootstrap';

<>
  <Card style={{ width: '18rem' }}>
    <Card.Header>Header</Card.Header>
    <Card.Img variant="top" src="image.png"/>
    <Card.Body>
      <Card.Title>Card Title</Card.Title>
      <Card.Subtitle className="mb-2 text-muted">Card Subtitle</Card.Subtitle>
      <Card.Text>
        Card example.
        This is a card's content.
      </Card.Text>
      <Card.Link href="#">Card Link</Card.Link>
    </Card.Body>
  </Card>
</>
```
- **적용 모습**

<img src="https://user-images.githubusercontent.com/55876471/147389349-7bc49a45-92ff-4500-9a29-a248c9344091.png" width="430" height="350"/>

-----
## Carousels
Carousel 컴포넌트를 이용하여 구성 요소를 순환시키는 슬라이드 쇼를 만들 수 있다.
이때 Carousel는 슬라이드 사이즈를 자동으로 정규화하지 않으므로, 사용자가 스타일을 정의하는 것이 필요하다.

- **코드**

  다음은 `<Carousel.Item>` 내에 interval 속성을 이용하여 슬라이드가 넘어가는 시간을 직접 정의한 예시이다.

```javascript
import { Carousel } from 'react-bootstrap';

<>
  <Carousel>
    <Carousel.Item interval={1500}>
      <img
        className="d-block w-100"
        src="img1.png"
        alt="First slide"
      />
      <Carousel.Caption>
        <h3>First slide label</h3>
        <p>This is a first slide show.</p>
      </Carousel.Caption>
    </Carousel.Item>
    <Carousel.Item interval={1500}>
      <img
        className="d-block w-100"
        src="img2.png"
        alt="Second slide"
      />
      <Carousel.Caption>
        <h3>Second slide label</h3>
        <p>This is a second slide show.</p>
      </Carousel.Caption>
    </Carousel.Item>
    <Carousel.Item interval={1500}>
      <img
        className="d-block w-100"
        src="img3.png"
        alt="Third slide"
      />
      <Carousel.Caption>
        <h3>Third slide label</h3>
        <p>This is a third slide show.</p>
      </Carousel.Caption>
    </Carousel.Item>
  </Carousel>
</>
```
- **적용 모습**

<img src="https://user-images.githubusercontent.com/55876471/147389874-afed5d88-a381-4cb6-8620-a4d38f2725e6.gif" width="400" height="250"/>

## Dropdowns
Dropdown은 링크 목록 등을 선택할 수 있는 토글 메뉴이다. Dropdown을 통한 메뉴 클릭 시 하위 메뉴가 나오게 된다.

- **코드**

  DropdownButton 클릭 시 Dropdown.Item에 담긴 목록들이 나온다.

```javascript
import { DropdownButton, Dropdown } from 'react-bootstrap';

<>
  <DropdownButton id="dropdown-basic-button" title="Dropdown Menu">
    <Dropdown.Item href="#/action-1">First Menu</Dropdown.Item>
    <Dropdown.Item href="#/action-2">Second Menu</Dropdown.Item>
    <Dropdown.Item href="#/action-3">Third Menu</Dropdown.Item>
    <Dropdown.Divider />
    <Dropdown.Item href="#/action-4">Separated Menu</Dropdown.Item>
  </DropdownButton>
</>
```
`<Dropdown.Driver />`를 이용하면 다음과 같이 하위 메뉴를 분리할 수 있다.

- **적용 모습**

<img src="https://user-images.githubusercontent.com/55876471/147390216-23623889-8904-47af-9fa3-7b3ea03a519e.gif" width="300" height="250"/>

-----
## Forms
Form 컴포넌트를 이용하여 입력 폼을 만들 수 있다. 회원가입/로그인 또는 파일 첨부 등의 입력 폼을 만들 때 자주 사용된다.

- **코드**

  다음은 Form 컴포넌트를 이용하여 이메일/비밀번호 입력 및 파일 첨부 폼을 만든 예시이다.

```javascript
import { Form } from 'react-bootstrap';

<>
  <Form>
    <Form.Group className="mb-3" controlId="EmailForm">
      <Form.Label>Email address</Form.Label>
      <Form.Control type="email" placeholder="id@example.com" />
    </Form.Group>
    <Form.Group className="mb-3" controlId="PasswordForm">
      <Form.Label>Password</Form.Label>
      <Form.Control type="password" placeholder="Password" />
    </Form.Group>
    <Form.Group controlId="formFile" className="mb-3">
      <Form.Label>file input</Form.Label>
      <Form.Control type="file" />
    </Form.Group>
  </Form>
</>
```

- **적용 모습**

<img src="https://user-images.githubusercontent.com/55876471/147390607-c1f8a8f6-dee3-49a6-a6bc-7ef73cc088d7.gif" width="550" height="320"/>

-----
## InputGroup
InputGroup과 FormControl 컴포넌트를 이용하여 입력 창을 구현할 수 있다.

- **코드**

  다음은 이름 및 학번을 입력받는 입력 창을 구현한 예시이다.

```javascript
import { InputGroup, FormControl } from 'react-bootstrap';

<>
  <InputGroup className="mb-3">
    <InputGroup.Text id="basic-addon1">이름</InputGroup.Text>
    <FormControl
      placeholder="name"
      aria-label="name"
      aria-describedby="basic-addon1"
    />
  </InputGroup>

  <InputGroup className="mb-3">
    <InputGroup.Text id="basic-addon1">학번</InputGroup.Text>
    <FormControl
      placeholder="student number"
      aria-label="student number"
      aria-describedby="basic-addon1"
    />
  </InputGroup>
</>
```

- **적용 모습**

<img src="https://user-images.githubusercontent.com/55876471/147481269-01e29156-fccc-4579-bb85-a1bf1f7aa651.gif" width="530" height="280"/>

-----
## List Groups
ListGroup 컴포넌트를 이용하여 일련의 내용을 표시하기 위한 그룹을 생성할 수 있다.

- **코드**

```javascript
import { ListGroup } from 'react-bootstrap';

<>
  <ListGroup>
    <ListGroup.Item>Item 1</ListGroup.Item>
    <ListGroup.Item>Item 2</ListGroup.Item>
    <ListGroup.Item>Item 3</ListGroup.Item>
    <ListGroup.Item>Item 4</ListGroup.Item>
    <ListGroup.Item>Item 5</ListGroup.Item>
  </ListGroup>
</>
```

- **적용 모습**

<img src="https://user-images.githubusercontent.com/55876471/147391009-431730cd-be8a-4e17-8cdc-ea6dbfe93497.png" width="500" height="280"/>

-----
## Modals
Modal 컴포넌트를 이용하여 사용자 알림, 사용자 지정 컨텐츠를 위한 대화상자를 띄울 수 있다.

- **코드**

  다음은 Modal 및 Button 컴포넌트를 이용하여, 버튼 클릭 시 Modal 창이 뜨도록 구현한 예시이다. 이때 Modal.Header 태그에 `closeButton` 속성을 적용하면 close 버튼을 생성할 수 있다.

```javascript
import { Modal, Button } from 'react-bootstrap';

const [show, setShow] = useState(false);
const handleClose = () => setShow(false);
const handleShow = () => setShow(true);

<>
  <Button variant="primary" onClick={handleShow}>
    Click me
  </Button>

  <Modal show={show} onHide={handleClose}>
    <Modal.Header closeButton>
      <Modal.Title>Modal Title</Modal.Title>
    </Modal.Header>
    <Modal.Body>This is a Modal Body!</Modal.Body>
    <Modal.Footer>
      <Button variant="primary" onClick={handleClose}>
        OK
      </Button>
    </Modal.Footer>
  </Modal>
</>
```

- **적용 모습**

<img src="https://user-images.githubusercontent.com/55876471/147391155-550a3c03-4b8f-4857-89e0-ecd9bb3fa278.gif" width="500" height="280"/>

-----
## Navbars
Navbar 컴포넌트를 이용하여 웹 페이지의 내비게이션 바를 구현할 수 있다. 주로 웹 페이지 상단의 메뉴 바를 만들 때 자주 사용된다.

- **코드**

  Navbar에서 `bg` 및 `variant` 속성을 변경하여 다음과 같은 색상의 내비게이션 바를 생성할 수 있다.

```javascript
import { Navbar, Container, Nav } from 'react-bootstrap';

<>
  <Navbar bg="light" variant="light">
    <Container>
    <Navbar.Brand href="#home">Navbar</Navbar.Brand>
    <Nav className="me-auto">
      <Nav.Link href="#home">Home</Nav.Link>
      <Nav.Link href="#link">Link</Nav.Link>
      <Nav.Link href="#mypage">My page</Nav.Link>
    </Nav>
    </Container>
  </Navbar>

  <Navbar bg="primary" variant="dark">
    <Container>
    <Navbar.Brand href="#home">Navbar</Navbar.Brand>
    <Nav className="me-auto">
      <Nav.Link href="#home">Home</Nav.Link>
      <Nav.Link href="#link">Link</Nav.Link>
      <Nav.Link href="#mypage">My page</Nav.Link>
    </Nav>
    </Container>
  </Navbar>

  <Navbar bg="dark" variant="dark">
    <Container>
    <Navbar.Brand href="#home">Navbar</Navbar.Brand>
    <Nav className="me-auto">
      <Nav.Link href="#home">Home</Nav.Link>
      <Nav.Link href="#link">Link</Nav.Link>
      <Nav.Link href="#mypage">My page</Nav.Link>
    </Nav>
    </Container>
  </Navbar>
</>

```

- **적용 모습**

<img src="https://user-images.githubusercontent.com/55876471/147402397-9402dcd1-77f9-48c9-99a8-70779195c68f.png" width="850" height="250"/>

-----
## Offcanvas
Offcanvas 컴포넌트를 이용하여 숨겨진 사이드바(sidebars)를 생성할 수 있다.
Offcanvas는 닫기 버튼이 있는 헤더를 제공하므로, close 버튼을 추가적으로 생성할 필요가 없다.

- **코드**

```javascript
import { Offcanvas, Button } from 'react-bootstrap';

const [show, setShow] = useState(false);
const handleClose = () => setShow(false);
const handleShow = () => setShow(true);

<>
  <Button variant="primary" onClick={handleShow}>
    Click me
  </Button>

  <Offcanvas show={show} onHide={handleClose} placement="start">
    <Offcanvas.Header closeButton>
      <Offcanvas.Title>Offcanvas</Offcanvas.Title>
    </Offcanvas.Header>
    <Offcanvas.Body>
      This is a Offcanvas example.
    </Offcanvas.Body>
  </Offcanvas>
</>
```
- **적용 모습**

  Offcanvas 컴포넌트의 `placement` 속성을 이용하여 사이드바가 나타나는 위치를 변경할 수 있다.

  - `start` : 왼쪽에서 사이드바가 나타난다.
  <img src="https://user-images.githubusercontent.com/55876471/147402859-54f06364-dddd-41f9-bf08-deae99303404.gif" width="400" height="340"/>

  - `end` : 오른쪽에서 사이드바가 나타난다.
  <img src="https://user-images.githubusercontent.com/55876471/147480558-4a3b7a2b-93a0-4884-8ecc-8206328eec4f.gif" width="400" height="340"/>

  - `top` : 위쪽에서 사이드바가 나타난다.
  <img src="https://user-images.githubusercontent.com/55876471/147402991-4fc5fc3d-7d15-46ae-8f8c-69616dd1bd8a.gif" width="400" height="340"/>

  - `bottom` : 아래쪽에서 사이드바가 나타난다.
  <img src="https://user-images.githubusercontent.com/55876471/147403117-021b5ef4-a3c7-4a89-b973-ed4543461d85.gif" width="400" height="340"/>

-----
## Progress bars
ProgressBar 컴포넌트를 이용하여 작업에 대한 진행률을 나타낼 수 있다.
- `now` : progress bar의 진행률에 대한 값을 나타낸다.
- `label` : progress bar의 진행률에 대한 퍼센트 값을 표시한다.
- `striped` : progress bar의 스트라이프 효과를 만들어낸다.
- `variant` : progress bar의 색상을 변경할 수 있다. ([Button](#buttons) 컴포넌트의 variant 속성과 동일하게 사용한다.)
- **코드**

```javascript
import { ProgressBar } from 'react-bootstrap';

<>
  <ProgressBar now={70} />

  <ProgressBar now={70} label="70%" />

  <ProgressBar striped now={70} label="70%" />

  <ProgressBar striped variant="success" now={70} />

  <ProgressBar striped variant="info" now={70} />

  <ProgressBar variant="warning" now={70} />

  <ProgressBar variant="danger" now={70} />
</>
```

- **적용 모습**

<img src="https://user-images.githubusercontent.com/55876471/147411141-c7603e6c-c411-4a89-819f-837987f89302.png" width="800" height="250"/>

-----
## Spinners
Spinner 컴포넌트를 이용하여 웹 페이지의 로딩 상태를 표시할 수 있다.
- `animation` : `border` 또는 `grow` 두 가지의 에니메이션 스타일을 사용할 수 있다.
- `variant` : spinner의 색상을 변경할 수 있다. ([Button](#buttons) 컴포넌트의 variant 속성과 동일하게 사용한다.)

- **코드**

  다음은 `animation`, `variant` 속성을 이용하여 spinner를 생성한 예시이다.

```javascript
import { Spinner } from 'react-bootstrap';

<>
  <Spinner animation="border"/>
  <Spinner animation="grow"/>

  <Spinner animation="border" variant="primary"/>
  <Spinner animation="grow" variant="primary"/>

  <Spinner animation="border" variant="warning"/>
  <Spinner animation="grow" variant="warning"/>
</>
```
- **적용 모습**

![Spinner](https://user-images.githubusercontent.com/55876471/147417377-10da9835-fd0c-4db0-bd6b-e56161fac582.gif)

-----
## Tables
Table 컴포넌트를 이용하여 표를 생성할 수 있다. `striped`, `bordered`, `hover` 속성을 이용하여 표를 사용자가 원하는 스타일에 맞게 만들 수 있다.

- **코드**

```javascript
import { Table } from 'react-bootstrap';

<>
  <Table striped bordered hover>
    <thead>
      <tr>
        <th>#</th>
        <th>First Name</th>
        <th>Last Name</th>
        <th>Email</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>1</td>
        <td>Chulsoo</td>
        <td>Kim</td>
        <td>ksh@example.com</td>
      </tr>
      <tr>
        <td>2</td>
        <td>Younghee</td>
        <td>Kim</td>
        <td>kyh@example.com</td>
      </tr>
      <tr>
        <td>3</td>
        <td>Seojoon</td>
        <td>Park</td>
        <td>psj@example.com</td>
      </tr>
    </tbody>
  </Table>
</>
```

- **적용 모습**

<img src="https://user-images.githubusercontent.com/55876471/147417799-902fc2b2-e774-4367-9540-1e7a428e3425.png" width="700" height="200"/>

-----
## Tabs
Tabs 및 Tab 컴포넌트를 이용하여 탭 메뉴를 생성할 수 있다.

- **코드**

  다음은 `Tabs`, `Tab` 컴포넌트를 이용하여 3개의 탭으로 구성된 탭 메뉴를 구현한 예시이다.

```javascript
import { Tabs, Tab } from 'react-bootstrap';

const [key, setKey] = useState('Tab 1');
<>
  <Tabs
    id="controlled-tab-example"
    activeKey={key}
    onSelect={(k) => setKey(k)}
    className="mb-3"
  >
    <Tab eventKey="Tab 1" title="Tab 1">
      Hi, This is Tab1.
    </Tab>
    <Tab eventKey="Tab 2" title="Tab 2">
      Hi, This is Tab2.
    </Tab>
    <Tab eventKey="Tab 3" title="Tab 3">
      Hi, This is Tab3.
    </Tab>
  </Tabs>
</>
```

- **적용 모습**

<img src="https://user-images.githubusercontent.com/55876471/147483588-73c4143c-f4a3-49e9-a00a-ba7cd101e422.gif" width="650" height="280"/>

- **코드**

  다음은 `TabContainer`, `TabContent`, `TabPane` 컴포넌트 및 `Nav`를 함께 이용하여 3개의 탭으로 구성된 탭 메뉴를 구현한 예시이다.

```javascript
import { Tab, Col, Row } from 'react-bootstrap';

<>
  <Tab.Container id="left-tabs-example" defaultActiveKey="first">
    <Row>
      <Col sm={3}>
        <Nav variant="pills" className="flex-column">
          <Nav.Item>
            <Nav.Link eventKey="first">Tab 1</Nav.Link>
          </Nav.Item>
          <Nav.Item>
            <Nav.Link eventKey="second">Tab 2</Nav.Link>
          </Nav.Item>
          <Nav.Item>
            <Nav.Link eventKey="third">Tab 3</Nav.Link>
          </Nav.Item>
        </Nav>
      </Col>
      <Col sm={9}>
        <Tab.Content>
          <Tab.Pane eventKey="first">
            Hi, This is Tab1.
          </Tab.Pane>
          <Tab.Pane eventKey="second">
            Hi, This is Tab2.
          </Tab.Pane>
          <Tab.Pane eventKey="third">
            Hi, This is Tab3.
          </Tab.Pane>
        </Tab.Content>
      </Col>
    </Row>
  </Tab.Container>
</>
```

- **적용 모습**

<img src="https://user-images.githubusercontent.com/55876471/147484610-bd252d60-628b-45af-bcaa-a59df2da6f73.gif" width="600" height="250"/>
