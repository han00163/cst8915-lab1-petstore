# CST8915 Lab 1: Algonquin Pet Store on Azure VM

**Student Name**: Dapeng/David Han

**Student ID**: 041-290-819

**Course**: CST8915 Full-stack Cloud-native Development

**Semester**: Fall 2026

---

## Demo Video

🎥 (https://youtu.be/om9WLKCRTJY)

---

## Technical Explanations

### Order Service (Node.js)

**Purpose:** Order service is responsible for receiving customer orders and send them to RabbitMQ for processing. 

**Technology Stack:** Order service is using JavaScript on top of Node.js,  Express to expose POST/orders endpoint on port 3000, and RabbitMQ for communication.

**Architecture Role:** Order service serves as input of order API and produce messages to RabbitMQ.

**Inter-Service Communication:** When end users submit order, the request is translated into JSON format and connected to RabbitMQ. 



### Product Service (Rust)

**Purpose:** Product service provides the product information to be displayed by the Store Front. 

**Technology Stack:** Product service uses Rust, the Warp framework for http routing, Tokio as asynchronous runtime and serde_json for JSON response. 

**Architecture Role:** Product service serves as API for Store Front HTTP GET request. 

**Inter-Service Communication:** Product service receives Store Front HTTP GET request and responses with product information.

### Store Front (Vue.js)

**Purpose:** Store front is the UI layer for this application. 

**Technology Stack:** Store front is based on Vue.js, JavaScript, HTML, CSS. 

**Architecture Role:** Store front is the UI layer of this application. 

**Inter-Service Communication:** Store front sends HTTP GET request to Product Service API and receives response before displaying the response. It also send HTTP POST request to Order Service. 






---

## Challenges and Learnings (Optional)

[Share any interesting challenges you faced during setup, how you solved them,
and what you learned from this lab experience]

---

## Acknowledgments

[Optional: Credit any resources, documentation, or people who helped you]