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

