## 1. 导航栏

```HTML
<nav class="navbar navbar-expand-sm navbar-dark bg-dark">
  #navbar-expand-sm: 响应式导航栏
  #navbar-dark: 导航栏黑色
  #bg-dark: 背景黑色
        <div class="container">
            <a href="index.html" class="navbar-brand">Glozzom</a>
            <button class="navbar-toggler" data-toggle="collapse" data-target="#navbarCollapse">
              #折叠导航栏
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarCollapse">
                <ul class="navbar-nav ml-auto">
                  #ml-auto: 导航栏的links显示在右侧
                    <li class="nav-item active">
                        <a href="index.html" class="nav-link">Home</a>
                    </li>
                    <li class="nav-item">
                        <a href="about.html" class="nav-link">About Us</a>
                    </li>
                    <li class="nav-item">
                        <a href="services.html" class="nav-link">Services</a>
                    </li>
                    <li class="nav-item">
                        <a href="blog.html" class="nav-link">Blog</a>
                    </li>
                    <li class="nav-item">
                        <a href="contact.html" class="nav-link">Contact</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

CSS:
.navbar .nav-link {
  font-size: 14px;
  text-transform: uppercase;
  padding-left: 1rem !important;
  padding-right: 1rem !important;
}

.navbar .nav-item.active {
  border-left: #444 3px solid;
}
```



## 2. Showcase Slider 轮播图

```html
<section id="showcase">
        <div id="myCarousel" class="carousel slide" data-ride="carousel">
          #class="carousel slide", data-ride="carousel"轮播的固定写法
          #id="myCarousel": 自己定义id，下面data-target即这个id
          #class="carousel-indicators": 固定写法, 轮播的指示符, 这里用了三个
          #class="carousel-inner": 轮播图片
          #class="carousel-caption": 在轮播图片上添加描述
          #data-slide="prev", class="carousel-control-prev": 添加左切换按钮
          #class="carousel-control-prev-icon": 左切换按钮图标
          #data-slide="next", class="carousel-control-next": 添加右切换按钮
          #class="carousel-control-next-icon": 右切换按钮图标
          #ul, ol区别: ul中用li, 显示文字前小黑点； ol中用li, 显示文字前是数字
            <ol class="carousel-indicators">
                <li data-target="#myCarousel" data-slide-to="0" class="active"></li>
                <li data-target="#myCarousel" data-slide-to="1"></li>
                <li data-target="#myCarousel" data-slide-to="2"></li>
            </ol>
            <div class="carousel-inner">
                <div class="carousel-item carousel-image-1 active">
                    <div class="container">
                        <div class="carousel-caption d-none d-sm-block text-right mb-5">
                            <h1 class="display-3">Heading One</h1>
                            <p class="lead">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Facilis iure dolorum culpa, sequi quibusdam dicta at voluptate atque rem ut.</p>
                            <a href="#" class="btn btn-danger btn-lg">Sign Up Now</a>
                        </div>
                    </div>
                </div>            

						<div class="carousel-item carousel-image-2">
                <div class="container">
                    <div class="carousel-caption d-none d-sm-block mb-5">
                        <h1 class="display-3">Heading Two</h1>
                        <p class="lead">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Facilis iure dolorum culpa, sequi quibusdam dicta at voluptate atque rem ut.</p>
                        <a href="#" class="btn btn-primary btn-lg">Learn More</a>
                    </div>
                </div>
            </div>

            <div class="carousel-item carousel-image-3">
                <div class="container">
                    <div class="carousel-caption d-none d-sm-block text-right mb-5">
                        <h1 class="display-3">Heading Three</h1>
                        <p class="lead">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Facilis iure dolorum culpa, sequi quibusdam dicta at voluptate atque rem ut.</p>
                        <a href="#" class="btn btn-success btn-lg">Learn More</a>
                    </div>
                </div>
            </div>
        </div>
        <a href="#myCarousel" data-slide="prev" class="carousel-control-prev">
            <span class="carousel-control-prev-icon"></span>
        </a>

        <a href="#myCarousel" data-slide="next" class="carousel-control-next">
            <span class="carousel-control-next-icon"></span>
        </a>
    </div>
</section>


CSS:
.carousel-item {
  height: 450px;
}

.carousel-image-1 {
  background: url('../img/image1.jpg');
  background-size: cover;
}

.carousel-image-2 {
  background: url('../img/image2.jpg');
  background-size: cover;
}


.carousel-image-3 {
  background: url('../img/image3.jpg');
  background-size: cover;
}
```


## 3. Home Icon Section



## 4. Home Heading Section