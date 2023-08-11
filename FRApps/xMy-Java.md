----
### 1. Copy 5c-my-react-app to 6c-my-custom-app 0:05
----

1. Right click on the client/5c-my-react-app folder and click Copy

![FRApps-Clone69](images/fr0103-FRApps-Clone-69.png "FRApps-Clone-69")


2. Right click on the client/5c-my-react-app folder and click Paste

![FRApps-Clone69](images/fr0103-FRApps-Clone-69-1.png "FRApps-Clone-69")


3. Right click on the client/5c-my-react-app-copy folder and click Rename

![FRApps-Clone69](images/fr0103-FRApps-Clone-69-2.png "FRApps-Clone-69")

- Enter:

```
6c-my-custom-app
```

![FRApps-Clone69](images/fr0103-FRApps-Clone-69-3.png "FRApps-Clone-69")

4. From 6c-my-custom-app folder, click to open the .env file

![FRApps-Clone69](images/fr0103-FRApps-Clone-69-4.png "FRApps-Clone-69")

- Change PORT to 50166

```
PORT=50166
```
![FRApps-Clone69](images/fr0103-FRApps-Clone-69-5.png "FRApps-Clone-69")

5. From 6c-my-custom-app folder, click toopen the package.json file

![FRApps-Clone69](images/fr0103-FRApps-Clone-69-6.png "FRApps-Clone-69")

- Make the following 3 changes

```
  "name": "6c-my-custom-app",

  "homepage": "/6c-my-custom-app",

   "prod": "node serveProd.js 51166",
```

![FRApps-Clone69](images/fr0103-FRApps-Clone-69-7.png "FRApps-Clone-69")

6. From 6c-my-custom-app/public folder, click to open the index.html file

![FRApps-Clone69](images/fr0103-FRApps-Clone-69-8.png "FRApps-Clone-69")

- Change the title

```
    <title>My Custom App</title>
```

![FRApps-Clone69](images/fr0103-FRApps-Clone-69-9.png "FRApps-Clone-69")




----
### 2. Run Client 6c-my-custom-app application 0:05
----

1. Right click on the client/6c-my-custom-app folder
2. Click Open in Integrated Terminal and click in the Terminal window, then enter 

![FRApps-Custom-01](images/fr0103-FRApps-Custom-01.png "FRApps-Custom-01") 

```
npm start
```

![FRApps-Custom-01a](images/fr0103-FRApps-Custom-01a.png "FRApps-Custom-01a")

- If you are prompted, click Allow Access

![FRApps-Clone-22a](images/fr0103-FRApps-Clone-22a.png "FRApps-Clone-22a")

![FRApps-Custom-01b](images/fr0103-FRApps-Custom-01b.png "FRApps-Custom-01b")

![FRApps-Custom-01c](images/fr0103-FRApps-Custom-01c.png "FRApps-Custom-01c")

----
### 3. Install and test React-Bootstrap and BootStrap libraries 0:05
----

[React-Bootstrap Reference](https://react-bootstrap.github.io/forms/overview/)

<br/>

1. Right click on the client/ folder
2. Click Open in Integrated Terminal and click in the Terminal window, then enter 

![FRApps-Custom-02](images/fr0103-FRApps-Custom-02.png "FRApps-Custom-02")


```
npm install react-bootstrap 
```

![FRApps-Custom-02](images/fr0103-FRApps-Custom-02a.png "FRApps-Custom-02")

3. In terminal Enter

```
npm install bootstrap
```

![FRApps-Custom-02](images/fr0103-FRApps-Custom-02a1.png "FRApps-Custom-02")

4. Check for production vulnerabilities

```
npm audit --production
```

![FRApps-Custom-02](images/fr0103-FRApps-Custom-02b.png "FRApps-Custom-02")

### 5. Add a Primary Button 0:05

<br/>

- Open src/App.js and add the following import statements to App.js

```
import Button from 'react-bootstrap/Button';
import "bootstrap/dist/css/bootstrap.css";
```

- Remove this import statement

```
import "./App.css";
```


![FRApps-Custom-02](images/fr0103-FRApps-Custom-02c.png "FRApps-Custom-02")

- Add the following code snippet to App.js

```
      <p>
        <Button variant="primary">
          Primary Button
        </Button>
      </p>
```

![FRApps-Custom-02](images/fr0103-FRApps-Custom-02d.png "FRApps-Custom-02")


6. Run or refresh http://localhost:50166/6c-my-custom-app on your browser

![FRApps-Custom-02](images/fr0103-FRApps-Custom-02e.png "FRApps-Custom-02")


----
### 6. Add Carousel component 0:05
----

[Carousel Sample](https://codesandbox.io/s/carousel-9vhdv2?file=/src/App.js)

<br/>

1. Open src/App.js and add the following import statements to App.js

```
import Carousel from "react-bootstrap/Carousel";
import Image from 'react-bootstrap/Image'
```

![FRApps-Custom-03](images/fr0103-FRApps-Custom-03c.png "FRApps-Custom-03")

2. Add the following code snippet to App.js

```
      <div>
        <Carousel>
          <Carousel.Item interval={500}>
            <Image
              className="d-block w-100"
              src="https://iso.500px.com/wp-content/uploads/2016/02/stock-photo-114337435.jpg"
              alt="First Slide"
              roundedCircle
            />
            <Carousel.Caption>
              <h3>Label for first slide</h3>
              <p>Sample Text for Image One</p>
            </Carousel.Caption>
          </Carousel.Item>
          <Carousel.Item interval={500}>
            <Image
              className="d-block w-100"
              src="https://iso.500px.com/wp-content/uploads/2016/03/stock-photo-142984111.jpg"
              alt="Second Slide"
            />
            <Carousel.Caption>
              <h3>Label for second slide</h3>
              <p>Sample Text for Image Two</p>
            </Carousel.Caption>
          </Carousel.Item>
        </Carousel>
      </div>
```

![FRApps-Custom-03](images/fr0103-FRApps-Custom-03d.png "FRApps-Custom-03")


3. Run or refresh http://localhost:50166/6c-my-custom-app on your browser

![FRApps-Custom-03](images/fr0103-FRApps-Custom-03e.png "FRApps-Custom-03")


### 7. Add Nav component 0:05
----

[Nav Sample](https://codesandbox.io/s/carousel-9vhdv2?file=/src/App.js)

<br/>

1. Open src/App.js and add the following import statements to App.js

```
import Carousel from "react-bootstrap/Carousel";
import Image from 'react-bootstrap/Image'
```

![FRApps-Custom-03](images/fr0103-FRApps-Custom-03c.png "FRApps-Custom-03")

2. Add the following code snippet to App.js

```
      <div>
        <Carousel>
          <Carousel.Item interval={500}>
            <Image
              className="d-block w-100"
              src="https://iso.500px.com/wp-content/uploads/2016/02/stock-photo-114337435.jpg"
              alt="First Slide"
              roundedCircle
            />
            <Carousel.Caption>
              <h3>Label for first slide</h3>
              <p>Sample Text for Image One</p>
            </Carousel.Caption>
          </Carousel.Item>
          <Carousel.Item interval={500}>
            <Image
              className="d-block w-100"
              src="https://iso.500px.com/wp-content/uploads/2016/03/stock-photo-142984111.jpg"
              alt="Second Slide"
            />
            <Carousel.Caption>
              <h3>Label for second slide</h3>
              <p>Sample Text for Image Two</p>
            </Carousel.Caption>
          </Carousel.Item>
        </Carousel>
      </div>
```

![FRApps-Custom-03](images/fr0103-FRApps-Custom-03d.png "FRApps-Custom-03")


3. Run or refresh http://localhost:50166/6c-my-custom-app on your browser

![FRApps-Custom-03](images/fr0103-FRApps-Custom-03e.png "FRApps-Custom-03")
