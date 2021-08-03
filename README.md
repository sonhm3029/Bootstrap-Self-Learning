# Bootstrap-Self-Learning
learning bootstrap my self in w3school
## Important components that need to notice:
- Buttons
- Collapse and dropdown
    * For build in collapse navbar of dropdown
- Colors
- Container
- Grid
- Jumbotron:
    * For the main image of header image
- list-group
- Navbar and nav:
    * For the header of page
- pagination:
    * For the navigation bars to next of previous page
- table
- form
- input
- carousel
===================================================
## About Collapse, Dropdown and their application
### 1. Drop down
- Đầu tiên bọc tất cả trong một `<div>` tag hoặc `<li>` tag tùy trường hợp với `class="dropdown"` để khi click, **dropdown** sẽ hiện ra ở chỗ button đó 
- Tiếp theo là phần button **dropdown**, nó có thể là một `<a>` hoặc là `<button>` với `class = "dropdown-toggler"` (để nó hiện ra biểu tượng drop down ở button đó) và `data-toggle = "dropdown"`...
- Cuối cùng là phần list **dropdown** sẽ hiện ra với `<div class="dropdown-menu">` và các `<a class="dropdown-item">` bên trong...

**Ví dụ:**
```
	<div class="dropdown">
  		<button class="dropdown-toggler" data-toggle='dropdown'>
    	<div class="dropdown-menu">
        	<div class="dropdown-header">Header 1</div>
        	<a class="dropdown-item">Link 1</a>
            <div class="dropdown-divider"></div>
            <a class="dropdown-item">Link 2</a>
        </div>
  	</div>
```
- The `dropdown-header` and `dropdown-divider` class use to add header and line in dropdown menu.

That's all.

======================================================
### 2. Collapse
- A basic collapse include of 2 part:
	- Thứ nhất là một `button` tag với `data-toggle="collapse"` và `data-targer=#idTarget"`. Trong đó idTarget là id của element muốn collapse
	- Thứ hai là element muốn collapse, ví dụ một `div` tag có `class="collapse"` và `id="idTarget"`.
- Default thì nội dung của element muốn collapse sẽ hide, thêm `class="show"` thì ban đầu nội dung sẽ đc **show**.

**Ví Dụ**
```
	<div class="container"">
    	<button data-toggle="collapse" data-target="#idTarget">Hide</button>
        <p class="collapse show" id="idTarget">This is collapsible paragraph</p>
    </div>
```
<br>
**Note**: Đối với `<a>` tag thì có thể thay `data-target` = `href`

<br>=> Việc sử dụng **Collapse** thích hợp trong việc tạo **_responsive navbar_**, menu **_navbar_** sẽ tự động collapse khi web load trên device có screen nhỏ. Hoặc sử dụng với `<card>` để tạo `accordion`.

======================================================
### 3.Navs
- Create `nav` include:
	-  `<ul>` tag với `class="nav"` với `<li class="nav-item">` và `<a class="nav-		link"` bên trong
	-  Ta có thể align `nav` với class `.justify-content-end/center` trong `<ul>`.
	-  Có thể định dạng `nav` với `<ul class="nav nav-tabs">` và `active` class để highligh **nav-item** đang được chọn.
	-  Có thể biến `nav` thành Toggleable/Dynamic Tabs.

**Ví dụ:**
```
<ul class="nav nav-tabs">
  <li class="nav-item">
    <a class="nav-link active" data-toggle="tab" href="#home">Home</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" data-toggle="tab" href="#menu1">Menu 1</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" data-toggle="tab" href="#menu2">Menu 2</a>
  </li>
</ul>

<!-- Tab panes -->
<div class="tab-content">
  <div class="tab-pane container active" id="home">...</div>
  <div class="tab-pane container fade" id="menu1">...</div>
  <div class="tab-pane container fade" id="menu2">...</div>
</div>
```
======================================================
## 4. Navbar
Từ những **component** trên ta tạo được **navbar** dùng làm header của page:
```
<nav class="navbar navbar-expand-md bg-dark navbar-dark">
                    <div class="container">
                        <a class="navbar-brand" href="index.html"><h2>LOGO</h2></a>
                        <button type="button" class="navbar-toggler" data-toggle="collapse" data-target="#collapsibleNavbar">
                            <span class="navbar-toggler-icon"></span>
                        </button>
                        <div class="collapse navbar-collapse" id="collapsibleNavbar">
                            <ul class="navbar-nav">
                                <li class="nav-item">
                                    <a class="nav-link" href="#">Link</a>
                                </li>
                                <li class="nav-item">
                                    <a class="nav-link" href="#">Link</a>
                                </li>
                                <li class="nav-item dropdown">
                                    <a class="nav-link dropdown-toggle" href="#" data-toggle="dropdown">Link</a>
                                    <div class="dropdown-menu">
                                        <a class="dropdown-item" href="#">Test 1</a>
                                        <a class="dropdown-item" href="#">Test 2</a>
                                        <a class="dropdown-item" href="#">Test 3</a>
                                    </div>
                                </li>
                            </ul>
                        </div>
                    </div>
                </nav>
```
======================================================
## 5. Pagination
- Được tạo bởi `<ul class="pagination">`, bên trong là `<li class="page-item">` và `<a class="page-link">`
- Căn lề **pagination** bằng `class=justify-content-/center/end`.

**Ví dụ:**
```
			<ul class="pagination justify-content-center">
                <li class="page-item">
                    <a class="page-link" href="page1.html">Page 1</a>
                </li>
                <li class="page-item">
                    <a class="page-link" href="page2.html">Page 2</a>
                </li>
                <li class="page-item">
                    <a class="page-link" href="page3.html">Page 3</a>
                </li>
            </ul>
```
======================================================
## 6. Color
- Bootstrap có các class thêm color cho chữ là:
- 
```
.text-muted, .text-primary, .text-success, .text-info, .text-warning, .text-danger, .text-secondary, .text-white, .text-dark, .text-body (default body color/often black) and .text-light
```
- Màu background là:
```
.bg-primary, .bg-success, .bg-info, .bg-warning, .bg-danger, .bg-secondary, .bg-dark and .bg-light.
```
======================================================
## 7.Jumbotron
- Wrap content với `<div class="jumbotron"></div>` để specify content đặc biệt.
**Ví dụ**:
```
<div class="jumbotron">
  <h1>Bootstrap Tutorial</h1>
  <p>Bootstrap is the most popular HTML, CSS...</p>
</div>
```
```
<div class="jumbotron jumbotron-fluid">
  <div class="container">
    <h1>Bootstrap Tutorial</h1>
    <p>Bootstrap is the most popular HTML, CSS...</p>
  </div>
</div>
```
======================================================
## 8. Grid
The Bootstrap 4 grid system has five classes:

- `.col-` (extra small devices - screen width less than 576px)
- `.col-sm-` (small devices - screen width equal to or greater than 576px)
- `.col-md-` (medium devices - screen width equal to or greater than 768px)
- `.col-lg-` (large devices - screen width equal to or greater than 992px)
- `.col-xl-` (xlarge devices - screen width equal to or greater than 1200px)
The classes above can be combined to create more dynamic and flexible layouts.

Theo sau bởi các số `col-sm-12/2/3/4/6`... ví dụ với:
- 12: 100% width
- 6: 50% width

=> Sử dụng trong responsive design.

======================================================
## 9. Form
Bootstrap provide 2 types of form layouts
- Stacked (full-width) form
- inline form

Example for stacked form:
```
<form action="/action_page.php">
  <div class="form-group">
    <label for="email">Email address:</label>
    <input type="email" class="form-control" placeholder="Enter email" id="email">
  </div>
  <div class="form-group">
    <label for="pwd">Password:</label>
    <input type="password" class="form-control" placeholder="Enter password" id="pwd">
  </div>
  <div class="form-group form-check">
    <label class="form-check-label">
      <input class="form-check-input" type="checkbox"> Remember me
    </label>
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>
```
**Giải thích**: đầu tiên chúng ta sẽ tạo một `form` tag là container với `action=..` cái này có lẽ ta học sau.
- Trong `form` tag sẽ gồm các `div` tag với `class="form-group"` để có margin nhìn ok hơn.
- Trong `div class="form-group"` bao gồm:
	- một `label` tag để tạo label cho input.
	- một `input` tag với `type="email"` để ô input có định dạng là email, khi người dùng nhập sai cú pháp email sẽ có thông báo hiện ra. `class="form-control"` để có đúng định dạng của **form**, `placeholder` để thể hiện chỉ dẫn ô input.

**Với inline form**:
- thêm `class="form-inline"` vào `form` tag. Tuy nhiên nó chỉ áp dụng vs min screen=576px, nếu nhỏ hơn thì --> sẽ chuyển thành stack.
### Form Validation:
Dùng để tạo thông báo khi có gì đó sai hoặc thiếu trong form khi customer dùng form trc hoặc sau khi nhấn submit:
- `.was-validated` thêm vào `class` của `form` tag để hiện thông báo thiếu hay sai gì trc khi nhấn nút submit form. Kèm theo đó là 2 `div`:
	- `<div class="valid-feeback">Valid</div>`
	- `<div class="invalid-feedback">Please fill out this field</div>`

trong `.form-group` để hiển thị thông báo.

**ví dụ**:
```
<form action="/action_page.php" class="was-validated">
  <div class="form-group">
    <label for="uname">Username:</label>
    <input type="text" class="form-control" id="uname" placeholder="Enter username" name="uname" required>
    <div class="valid-feedback">Valid.</div>
    <div class="invalid-feedback">Please fill out this field.</div>
  </div>
  <div class="form-group">
    <label for="pwd">Password:</label>
    <input type="password" class="form-control" id="pwd" placeholder="Enter password" name="pswd" required>
    <div class="valid-feedback">Valid.</div>
    <div class="invalid-feedback">Please fill out this field.</div>
  </div>
  <div class="form-group form-check">
    <label class="form-check-label">
      <input class="form-check-input" type="checkbox" name="remember" required> I agree on blabla.
      <div class="valid-feedback">Valid.</div>
      <div class="invalid-feedback">Check this checkbox to continue.</div>
    </label>
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>
```

**==>** Form dùng để tạo giao diện điền mật khẩu tài khoản......

======================================================
## 10.Input
Các form control mà bootstrap support bao gồm:
- input
- textarea
- checkbox
- radio
- select

Kèm theo đó là các kiểu input : `type=`  _**text, password, datetime, datetime-local, date, month, time, week, number, email, url, search, tel, and color**_.

Như ví dụ với form, ta dùng `type=email` và `type=password`

**Note:** Inputs will NOT be fully styled if their type is not properly declared!<br>
**Ví dụ** với `textarea` để tạo comment box:
```
<form action="/action_page.php">
    <div class="form-group">
      <label for="comment">Comment:</label>
      <textarea class="form-control" rows="5" id="comment" name="text"></textarea>
    </div>
    <button type="submit" class="btn btn-primary">Submit</button>
</form>
```

**Ví dụ** với `checkbox`:
```
<div class="form-check">
  <label class="form-check-label">
    <input type="checkbox" class="form-check-input" value="">Option 1
  </label>
</div>
<div class="form-check">
  <label class="form-check-label">
    <input type="checkbox" class="form-check-input" value="">Option 2
  </label>
</div>
<div class="form-check">
  <label class="form-check-label">
    <input type="checkbox" class="form-check-input" value="" disabled>Option 3
  </label>
</div>
```

**Ví dụ** với `radio` check hình tròn:
```
<div class="form-check">
  <label class="form-check-label">
    <input type="radio" class="form-check-input" name="optradio">Option 1
  </label>
</div>
<div class="form-check">
  <label class="form-check-label">
    <input type="radio" class="form-check-input" name="optradio">Option 2
  </label>
</div>
<div class="form-check disabled">
  <label class="form-check-label">
    <input type="radio" class="form-check-input" name="optradio" disabled>Option 3
  </label>
</div>
```
**Ví dụ** với `select` list:
```
<div class="form-group">
  <label for="sel1">Select list:</label>
  <select class="form-control" id="sel1">
    <option>1</option>
    <option>2</option>
    <option>3</option>
    <option>4</option>
  </select>
</div>
```
- Đây là just one selection
- Muốn dùng multiple seclection (giữ control và chọn) thì thay `class="form-control"` trong `select` tag thành `multiple class="form-control"`

**Ví dụ** với input `file` và `range`:
```
<form action="/action_page.php">
    <div class="form-group">
      <input type="range" class="form-control-range" name="range">
    </div>
    <div class="form-group">
      <input type="file" class="form-control-file border" name="file">
    </div>
    <button type="submit" class="btn btn-primary">Submit</button>
 </form>
```
- Với type `range` là thanh kéo range input
- type `file` là input = mở tệp.

======================================================

## 11. Carousel
Create a slide show:

**Ví dụ**:
```
<div id="demo" class="carousel slide" data-ride="carousel">

  <!-- Indicators -->
  <ul class="carousel-indicators">
    <li data-target="#demo" data-slide-to="0" class="active"></li>
    <li data-target="#demo" data-slide-to="1"></li>
    <li data-target="#demo" data-slide-to="2"></li>
  </ul>

  <!-- The slideshow -->
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src="la.jpg" alt="Los Angeles">
    </div>
    <div class="carousel-item">
      <img src="chicago.jpg" alt="Chicago">
    </div>
    <div class="carousel-item">
      <img src="ny.jpg" alt="New York">
    </div>
  </div>

  <!-- Left and right controls -->
  <a class="carousel-control-prev" href="#demo" data-slide="prev">
    <span class="carousel-control-prev-icon"></span>
  </a>
  <a class="carousel-control-next" href="#demo" data-slide="next">
    <span class="carousel-control-next-icon"></span>
  </a>

</div>
```
**Giải thích:**

| Class					|					Description							|
| ----------------------|:-----------------------------------------------------:|
|.carousel				|Creates a carousel										|
|.carousel-indicators	|Adds indicators for the carousel. These are the little dots 						  at the bottom of each slide (which indicates how many slides 							there are in the carousel, and which slide the user are 							 currently viewing)										|
|.carousel-inner		|Adds slides to the carousel							|
|.carousel-item			|	Specifies the content of each slide					|
|.carousel-control-prev	|Adds a left (previous) button to the carousel, which allows 							the user to go back between the slides				 |
|.carousel-control-next	|Adds a right (next) button to the carousel, which allows the 							user to go forward between the slides				  |
|.carousel-control-prev-icon|Used together with .carousel-control-prev to create a								"previous" button
|.carousel-control-next-icon|Used together with .carousel-control-next to create a 								"next" button
|.slide					|Adds a CSS transition and animation effect when sliding from one item to the next. Remove this class if you do not want this effect


Add elements inside `<div class="carousel-caption">` within each `<div class="carousel-item">` to create a caption for each slide:
**Ví dụ:**

```
<div class="carousel-item">
  <img src="la.jpg" alt="Los Angeles">
  <div class="carousel-caption">
    <h3>Los Angeles</h3>
    <p>We had such a great time in LA!</p>
  </div>
</div>
```

======================================================
## 12. Modal




