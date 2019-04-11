## 1. 导航栏

```html
<nav class="navbar navbar-expand-sm bg-dark navbar-dark fixed-top">
  #navbar-expand-sm: 设置这个导航栏为响应式的，在不同设备上自动适应
  #bg-dark: 设置导航栏的背景为dark颜色
  #navbar-dark: 设置导航栏的文字为dark颜色
  #fixed-top: 设置导航栏固定在top位置
    <div class="container">
        <a href="index.html" class="navbar-brand">LoopLAB</a>
      	#navbar-brand: 类用于高亮显示品牌/Logo
        <button class="navbar-toggle" data-toggle="collapse" data-target="#navbarCollapse">
          #navbar-toggle, data-toggle: 设置折叠导航栏
          #data-target='#自己设置一个id名字'
            <span class="navbar-toggler-icon"></span>
          #navbar-toggler-icon: 折叠导航栏的图标
        </button>
        <div class="collapse navbar-collapse" id="navbarCollapse">
            #这里就是写折叠导航栏里的有哪些东西, 
          	#注意这里的id和上面那个设置折叠导航栏的id相同
          	#才说明这个是上面定义的那个折叠导航栏
          	<ul class="navbar-nav ml-auto">
                <li class="nav-item">
                    <a href="#home" class="nav-link">Home</a>
                </li>
                <li class="nav-item">
                    <a href="#explore-head-section" class="nav-link">Explore</a>
                </li>
                <li class="nav-item">
                    <a href="#create-head-section" class="nav-link">Create</a>
                </li>
                <li class="nav-item">
                    <a href="#share-head-section" class="nav-link">Share</a>
                </li>
            </ul>
        </div>
    </div>
</nav>

body {
  background: #333;  ->是指背景是黑色
  color: #fff;   ->Color属性指定文本的颜色 
}

.navbar {
  border-bottom: #008ed6 3px solid; ->border-bottom缩写属性设置一个声明中所有底部边框属性
  opacity: 0.8;  ->Opacity属性设置一个元素了透明度级别
}
```



## 2. Home section

```html
<!-- HOME SECTION -->
<header id="home-section">
    <div class="dark-overlay">
        <div class="home-inner container">
          #这里直接把container放在这里，或者再内嵌一个【<div class="container"></div>】 
            <div class="row">
                <div class="col-lg-8 d-none d-lg-block">
                  #隐藏元素, 当浏览器界面被缩小时.
                  #d-none d-lg-block: 表示当界面小于lg时，这部分会被隐藏.
                  #若只有d-none:表示这部分无论界面如何都被隐藏.
                    <h1 class="display-4">Build 
                        <strong>social profiles</strong> and gain revenue 
                        <strong>profits</strong>
                    </h1>
                    <div class="d-flex">
                      #弹性盒子布局【Bootstrap3与4最大的区别就是4使用弹性盒子来布局】
                        <div class="p-4 align-self-start">
                            <i class="fas fa-check fa-2x"></i>
                          	#使用Font Awesome里的图标
                        </div>
                        <div class="p-4 align-self-end">
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Necessitatibus eaque magni praesentium facere nemo vitae!
                        </div>
                    </div>
                    <div class="d-flex">
                        <div class="p-4 align-self-start">
                            <i class="fas fa-check fa-2x"></i>
                        </div>
                        <div class="p-4 align-self-end">
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Necessitatibus eaque magni praesentium facere nemo vitae!
                        </div>
                    </div>
                    <div class="d-flex">
                        <div class="p-4 align-self-start">
                            <i class="fas fa-check fa-2x"></i>
                        </div>
                        <div class="p-4 align-self-end">
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Necessitatibus eaque magni praesentium facere nemo vitae!
                        </div>
                    </div>
                </div>

                <div class="col-lg-4">
                  #同一个<div class="row">里, 上面的是在左col-lg-8个位置
                  #下面写的表格占右边col-lg-4个位置
                    <div class="card bg-primary text-center card-form">
                        <div class="card-body">
                            <h3>Sign Up Today</h3>
                            <p>Please fill out this form to register</p>
                            <form>
                              	#使用form表单
                                <div class="form-group">
                                    <input type="text" class="form-control form-control-lg" placeholder="Username">
                                </div>
                                <div class="form-group">
                                    <input type="email" class="form-control form-control-lg" placeholder="Email">
                                </div>
                                <div class="form-group">
                                    <input type="password" class="form-control form-control-lg" placeholder="Password">
                                </div>
                                <div class="form-group">                                                 
                                    <input type="password" class="form-control form-control-lg" placeholder="Confirm Password">
                                </div>
                                <input type="submit" value="submit" class="btn btn-outline-light btn-block">
                            </form>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</header>

知识点：
(1)background-size中，100%和cover都是用于将图片扩大或者缩放来适应整个容器
background-size：100% 100%;---按容器比例撑满，图片变形；
background-size：cover;---把背景图片放大到适合元素容器的尺寸，图片比例不变，但是要注意，超出容器的部分可能会裁掉
(2)如何设置一个固定的背景图像：
body
{ 
  background-image: url('smiley.gif');
  background-repeat: no-repeat;
  background-attachment: fixed;
}
  
  

CSS:
#home-section {
  background: url(../img/home.jpg);
  background-repeat: no-repeat;
  background-size: cover;   #把背景图片放大到适合元素容器的尺寸，图片比例不变
  background-attachment: fixed;   #设置固定的背景图像
  min-height: 700px;        #min-height 属性设置元素的最小高度。
}

#home-section .dark-overlay {
  position: absolute;    #用绝对定位,一个元素可以放在页面上的任何位置 top=0, left=0
  top: 0;
  left: 0;
  width: 100%;
  min-height: 700px;
  background-color: rgba(0, 0, 0, 0.7);   #rgba位置分别是GRB,最后一位是opacity程度
}

#home-section .home-inner {
  padding-top: 150px;    #padding-top属性设置一个元素的顶部填充
}

#home-section .card-form {
  opacity: 0.8;    #透明程度
}

#home-section .fas {
  color: #008ed6;      #text颜色
  background: #fff;    #背景颜色
  padding: 5px;        #设置元素的填充，若没有指定哪个方向则是四个方向都有
  border-radius: 5px;  #给div元素添加圆角的边框
}
```



## 3. Explore section


```html
<!-- EXPLORE HEAD -->
<section id="explore-head-section">
    <div class="container">
        <div class="row">
            <div class="col text-center py-5">
              	#py-5是啥...没搜到...
                <h1 class="display-4">Explore</h1>
                <p class="lead">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ab labore necessitatibus blanditiis maxime aspernatur, minima.</p>
                <a href="#" class="btn btn-outline-secondary">Find Out More</a>
              	#class="btn btn-outline-secondary"灰色的按钮，中间是空心
            </div>
        </div>
    </div>
</section>


<!-- EXPLORE SECTION -->
<section id="exploree-section" class="bg-light text-muted py-5">
  	#bg-light背景颜色, text-muted文字颜色
    <div class="container">
        <div class="row">
            <div class="col-md-6">
                <img src="img/explore-section1.jpg" alt="" class="img-fluid mb-3 rounded-circle">
            </div>
            <div class="col-md-6">
                <h3>Explore & Connect</h3>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dicta soluta, reiciendis officia doloribus fugit quam repellendus et maxime ducimus minima?</p>
                <div class="d-flex">
                    <div class="p-4 align-self-start">
                        <i class="fas fa-check fa-2x"></i>
                    </div>
                    <div class="p-4 align-self-end">
                        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Reprehenderit quis, obcaecati temporibus tempora cupiditate hic!
                    </div>
                </div>
                <div class="d-flex">
                    <div class="p-4 align-self-start">
                        <i class="fas fa-check fa-2x"></i>
                    </div>
                    <div class="p-4 align-self-end">
                        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Reprehenderit quis, obcaecati temporibus tempora cupiditate hic!
                    </div>
                </div>
            </div>
        </div>
    </div>
</section> 


CSS:
#explore-section .fas, #share-section .fas {
  background: #333;    #背景黑色
  color: #fff;         #text白色
  padding: 5px;				 #四周内边距5px
  border-radius: 5px;	 #给div元素添加圆角的边框
}
```



## 4. CREATE / SHARE


```html
<!-- CREATE HEAD -->
<section id="create-head-section" class="bg-primary">
    <div class="container">
        <div class="row">
            <div class="col text-center py-5">
                <h1 class="display-4">Create</h1>
                <p class="lead">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ab labore necessitatibus blanditiis maxime aspernatur, minima.</p>
                <a href="#" class="btn btn-outline-light">Find Out More</a>
            </div>
        </div>
    </div>
</section>


<!-- CREATE SECTION  -->
<section id="create-section" class="py-5">
    <div class="container">
        <div class="row">
            <div class="col-md-6 order-2">
                <img src="img/create-section1.jpg" alt="" class="img-fluid mb-3 rounded-circle">
            </div>
            <div class="col-md-6 order-1">
                <h3>Create Your Passion</h3>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dicta soluta, reiciendis officia doloribus fugit quam repellendus et maxime ducimus minima?</p>
                <div class="d-flex">
                    <div class="p-4 align-self-start">
                        <i class="fas fa-check fa-2x"></i>
                    </div>
                    <div class="p-4 align-self-end">
                        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Reprehenderit quis, obcaecati temporibus tempora cupiditate hic!
                    </div>
                </div>
                <div class="d-flex">
                    <div class="p-4 align-self-start">
                        <i class="fas fa-check fa-2x"></i>
                    </div>
                    <div class="p-4 align-self-end">
                        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Reprehenderit quis, obcaecati temporibus tempora cupiditate hic!
                    </div>
                </div>
            </div>
        </div>
    </div>
</section> 
```


```html
<!-- SHARE HEAD -->
<section id="share-head-section" class="bg-primary">
    <div class="container">
        <div class="row">
            <div class="col text-center py-5">
                <h1 class="display-4">Share</h1>
                <p class="lead">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ab labore necessitatibus blanditiis maxime aspernatur, minima.</p>
                <a href="#" class="btn btn-outline-light">Find Out More</a>
            </div>
        </div>
    </div>
</section>
```


```html
<!-- SHARE SECTION -->
<section id="share-section" class="bg-light text-muted py-5">
    <div class="container">
        <div class="row">
            <div class="col-md-6">
                <img src="img/share-section1.jpg" alt="" class="img-fluid mb-3 rounded-circle">
            </div>
            <div class="col-md-6">
                <h3>Share What You Create</h3>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dicta soluta, reiciendis officia doloribus fugit quam repellendus et maxime ducimus minima?</p>
                <div class="d-flex">
                    <div class="p-4 align-self-start">
                        <i class="fas fa-check fa-2x"></i>
                    </div>
                    <div class="p-4 align-self-end">
                        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Reprehenderit quis, obcaecati temporibus tempora cupiditate hic!
                    </div>
                </div>
                <div class="d-flex">
                    <div class="p-4 align-self-start">
                        <i class="fas fa-check fa-2x"></i>
                    </div>
                    <div class="p-4 align-self-end">
                        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Reprehenderit quis, obcaecati temporibus tempora cupiditate hic!
                    </div>
                </div>
            </div>
        </div>
    </div>
</section> 
```



## 5. FOOTER

```html
<!-- FOOTER -->
<footer id="main-footer" class="bg-dark">
    <div class="container">
        <div class="row">
            <div class="col text-center py-4">
                <h3>LoopLAB</h3>
                <p>Copyright &copy; <span id="year"></span></p>
                <button class="btn btn-primary" data-toggle="modal" data-target="#contactModal">Contact Us
                  #Modal(模态框,子窗口)
                  #data-toggle指以什么事件触发，常用的如collapse,modal,popover,tooltips等
                  #data-target指事件的目标
                  #一起使用就是代表data-target所指的元素以data-toggle指定的形式显示
                </button>
            </div>
        </div>
    </div>
</footer>


<!-- CONTACT MODAL -->
#modal模态框Modal
<div class="modal fade text-dark" id="contactModal">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title">Contact Us</h5>
        <button class="close" data-dismiss="modal">
          <span>&times;</span>
        </button>
      </div>
      <div class="modal-body">
        <form>
          <div class="form-group">
            <label for="name">Name</label>
            <input type="text" class="form-control">
          </div>
          <div class="form-group">
            <label for="email">Email</label>
            <input type="email" class="form-control">
          </div>
          <div class="form-group">
            <label for="message">Message</label>
            <textarea class="form-control"></textarea>
          </div>
        </form>
      </div>
      <div class="modal-footer">
        <button class="btn btn-primary btn-block">Submit</button>
        #btn-block: 块级按钮(拉伸至父元素100%的宽度)
      </div>
    </div>
  </div>
</div>
```



## 6. 滚动下拉

```javascript
<body data-spy="scroll" data-target="#main-nav" id="home">	
<nav class="navbar navbar-expand-sm bg-dark navbar-dark fixed-top" id="main-nav">
</nav>

<script>
    // Get the current year for the copyright
    $('#year').text(new Date().getFullYear());

    // Init Scrollspy
    $('body').scrollspy({ target: '#main-nav' });

    // Smooth Scrolling
    $("#main-nav a").on('click', function (event) {
        if (this.hash !== "") {
            event.preventDefault();
            const hash = this.hash;
            $('html, body').animate({
                scrollTop: $(hash).offset().top
            }, 800, function () {
                window.location.hash = hash;
            });
        }
    });
</script>
```