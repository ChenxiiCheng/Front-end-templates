# Mizuxe

## 1. 导航栏

```html
<nav class="navbar navbar-expand-md navbar-light fixed-top py-4">
  #navbar-expand-md: 设置响应式导航栏
  #navbar-light: 导航栏颜色为light
  #fixed-top: 导航栏固定在top
  #py-4: top和bottom padding=4
  <div class="container">
    <a href="#home" class="navbar-brand">
      <img src="img/mlogo.png" width="50" height="50" alt="">
      <h3 class="d-inline align-middle">Mizuxe</h3>
      #d-inline: 内联元素
      #align-middle: 没搜到，应该是放在中间吧
      #应该是等同于vertical-align: middle
    </a>
    <button class="navbar-toggler" data-toggle="collapse" data-target="#navbarCollapse">
      #可折叠式的导航栏，右边的button
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarCollapse">
      <ul class="navbar-nav ml-auto">
        #ml-auto: 放在右边
        <li class="nav-item">
          <a href="#home" class="nav-link">Home</a>
        </li>
        <li class="nav-item">
          <a href="#about" class="nav-link">About</a>
        </li>
        <li class="nav-item">
          <a href="#authors" class="nav-link">Meet The Authors</a>
        </li>
        <li class="nav-item">
          <a href="#contact" class="nav-link">Contact</a>
        </li>
      </ul>
    </div>
  </div>
</nav>


CSS:
$primary: #3292a6;
$primary-overlay: rgba(50, 146, 166, 0.8);

body {
	margin-top: 105px;
} 

.navbar {
	box-shadow: 2px 2px 5px $primary;  #向元素添加阴影：
	opacity: 0.9;						  #透明度
	background: #fff;         #背景白色

	.nav-item {
		font-size: 1.4rem;      #字体大小
		padding-right: 1.4rem;  #右内边距
	}
}
```


## 2. Showcase

```html
<!-- SHOWCASE -->
<section id="showcase" class="py-5">
  #py-5: top和bottom  padding=5px
    <div class="primary-overlay text-white">
      #文字设置成白色
        <div class="container">
            <div class="row">
                <div class="col-lg-6 text-center">
                    <h1 class="display-2 mt-5 pt-5">
                      #mt-5 pt-5: 没搜到....
                        Do What You Dream Of...
                    </h1>
                    <p class="lead">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Amet, incidunt?
                    </p>
                    <a href="#" class="btn btn-outline-secondary btn-lg text-white">
                        <i class="fas fa-arrow-right"></i>Read More
                      	#箭头符号
                    </a>
                </div>
                <div class="col-lg-6">
                    <img src="img/book.png" alt="" class="img-fluid d-none d-lg-block">
                  	#img-fluid: 根据页面大小自动适应图片大小
                  	#d-none, d-lg-block: 当界面小于lg时，看不见这张图了
                </div>
            </div>
        </div>
    </div>
</section>


CSS:
#showcase {
	position: relative;
	background: url('../img/mountains.jpg');
	min-height: 600px;

	.primary-overlay {
		background: $primary-overlay;   #设置颜色
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
	}
}
```


## 3. Newsletter

```html
<!-- NEWSLETTER -->
<section id="newsletter" class="bg-dark text-white py-5">
    <div class="container">
        <div class="row">
            <div class="col-md-4">
                <input type="text" class="form-control form-control-lg mb-resp" placeholder="Enter Name">
              	#form-control-lg: 想要大的form
              	#mb-resp: 当界面缩小是，显示上下关系，这个mb-resp在scss中写的，实现中间留一点空隙
            </div>
            <div class="col-md-4">
                <input type="email" class="form-control form-control-lg mb-resp" placeholder="Enter Email">
            </div>
            <div class="col-md-4">
                <button class="btn btn-primary btn-lg btn-block">
                    <i class="fas fa-envelope-open-o"></i> Subscribe    
                </button>
            </div>
        </div>
    </div>
</section>


@media(max-width: 768px) {
	#showcase {
		min-height: 500px;

		h1 {
			font-size: 4rem;
		}
	}

	.mb-resp {
		margin-bottom: 1rem;
	}
}
```


## 4. Boxes

```html
<!-- BOXES -->
<section id="boxes" class="py-5">
    <div class="container">
        <div class="row">
            <div class="col-md-3">
                <div class="card text-center border-primary mb-resp">
                  #bordeer-primary: 卡片边框border是primary的颜色，类似btn-primary那样
                    <div class="card-body">
                        <h3 class="text-primary">Be Better</h3>
                      	#text-primary: 类似btn-primary，字体变成primary这个颜色
                        <p class="text-muted">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Rem, sapiente!</p>
                      	#text-muted: 字体颜色为muted，类似btn-muted
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="card text-center bg-primary text-white mb-resp">
                  #bg-primary: 这个是背景变成primary这个颜色
                  #text-white: 字体白色
                    <div class="card-body">
                        <h3>Be Smarter</h3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Rem, sapiente!</p>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="card text-center border-primary mb-resp">
                    <div class="card-body">
                        <h3 class="text-primary">Be Faster</h3>
                        <p class="text-muted">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Rem, sapiente!</p>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="card text-center bg-primary text-white mb-resp">
                    <div class="card-body">
                        <h3>Be Stronger</h3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Rem, sapiente!</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

pb-3: ->padding-bottom-3
mb-0: ->margin-bottom-0
my-5: ->margin top and bottom 5px
w-50: ->width 50
```


## 5. About / Why section


```html
<section id="about" class="py-5 text-center bg-light">
        <div class="container">
            <div class="row">
                <div class="col">
                    <div class="info-header mb-5">
                      #mb-5: margin-botton = 5px
                        <h1 class="text-primary pb-3">
                          #文本设置成primary颜色， pading-bottom: 3px
                            Why This Book?
                        </h1>
                        <p class="lead pb-3">
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nesciunt unde laboriosam, ipsum exercitationem est dicta?
                        </p>
                    </div>  
                  	
                  	<!-- ACCORDION -->
                    <div id="accordion">
                        <div class="card">
                            <div class="card-header">
                                <h5 class="mb-0">
                                    <div href="#collapse1" data-toggle="collapse" data-parent="#accordion">
                                      #不加“data-parent”的话，再点击其他标题的时候，
                                      #此时点击的这个标题的内容还是展开的。
                                      #加上之后，只会显示当前所点击那个标题的内容
                                        <i class="fas fa-arrow-circle-down"></i> Get Inspired	
                                    </div>
                                </h5>
                            </div>

                            <div id="collapse1" class="collapse show">
                                <div class="card-body">
                                    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Provident nihil libero doloribus asperiores ea maxime facere placeat, molestiae, non magnam pariatur, iste ducimus ut quaerat, rem repudiandae incidunt ipsa necessitatibus! Adipisci quidem consectetur ad necessitatibus! Tenetur consequatur reiciendis dolorem temporibus provident, expedita at quisquam placeat mollitia, pariatur ad, iste libero.
                                </div>
                            </div>
                        </div>

                        <div class="card">
                            <div class="card-header">
                                <h5 class="mb-0">
                                    <div href="#collapse2" data-toggle="collapse" data-parent="#accordion">
                                        <i class="fas fa-arrow-circle-down"></i> Gain The Knowledge
                                    </div>
                                </h5>
                            </div>

                            <div id="collapse2" class="collapse">
                                <div class="card-body">
                                    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Provident nihil libero doloribus asperiores ea maxime facere placeat, molestiae, non magnam pariatur, iste ducimus ut quaerat, rem repudiandae incidunt ipsa necessitatibus! Adipisci quidem consectetur ad necessitatibus! Tenetur consequatur reiciendis dolorem temporibus provident, expedita at quisquam placeat mollitia, pariatur ad, iste libero.
                                </div>
                            </div>
                        </div>

                        <div class="card">
                            <div class="card-header">
                                <h5 class="mb-0">
                                    <div href="#collapse3" data-toggle="collapse" data-parent="#accordion">
                                        <i class="fas fa-arrow-circle-down"></i> Open Your Mind
                                    </div>
                                </h5>
                            </div>

                            <div id="collapse3" class="collapse">
                                <div class="card-body">
                                    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Provident nihil libero doloribus asperiores ea maxime facere placeat, molestiae, non magnam pariatur, iste ducimus ut quaerat, rem repudiandae incidunt ipsa necessitatibus! Adipisci quidem consectetur ad necessitatibus! Tenetur consequatur reiciendis dolorem temporibus provident, expedita at quisquam placeat mollitia, pariatur ad, iste libero.
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
								
```


## 6. Authors

```html
<section id="authors" class="my-5 text-center">
  			#my-5: margin top and bottom 5px
        <div class="container">
            <div class="row">
                <div class="col">
                    <div class="info-header mb-5">
                      #mb-5: margin-bottom 5px
                        <h1 class="text-primary pb-3">
                          #pb-3: padding-bottom 3px
                            Meet The Authors
                        </h1>
                        <p class="lead">
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Esse architecto dolores doloremque, magni fugiat, suscipit.
                        </p>
                    </div>
                </div>
            </div>
            
            <div class="row">
                <div class="col-lg-3 col-md-6">
                  	#当界面是lg时每个占3个col，所以总共显示4个
                  	#当界面是md时每个站6个col，所以总共显示2个
                    <div class="card">
                        <div class="card-body">
                            <img src="img/person1.jpg" alt="" class="img-fluid rounded-circle w-50 mb-3">
                          #img-fluid: 图片根据界面自适应大小
                          #rounded-circle: 图片弄成圆形
                          #w-50: width 50
                          #mb-3: margin-bottom 3px
                            <h3>Susan Williams</h3>
                            <h5 class="text-muted">Lead Writer</h5>
                            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eius obcaecati veritatis aut perferendis harum numquam?</p>
                            <div class="d-flex justify-content-center">
                                <div class="p-4">
                                    <a href="http://facebook.com">
                                        <i class="fab fa-facebook"></i>
                                    </a>
                                </div>
                                <div class="p-4">
                                    <a href="http://twitter.com">
                                        <i class="fab fa-twitter"></i>
                                    </a>
                                </div>
                                <div class="p-4">
                                    <a href="http://instagram.com">
                                        <i class="fab fa-instagram"></i>
                                    </a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="col-lg-3 col-md-6">
                    <div class="card">
                        <div class="card-body">
                            <img src="img/person2.jpg" alt="" class="img-fluid rounded-circle w-50 mb-3">
                            <h3>Grace Smith</h3>
                            <h5 class="text-muted">Co-Writer</h5>
                            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eius obcaecati veritatis aut perferendis harum numquam?</p>
                            <div class="d-flex justify-content-center">
                                <div class="p-4">
                                    <a href="http://facebook.com">
                                        <i class="fab fa-facebook"></i>
                                    </a>
                                </div>
                                <div class="p-4">
                                    <a href="http://twitter.com">
                                        <i class="fab fa-twitter"></i>
                                    </a>
                                </div>
                                <div class="p-4">
                                    <a href="http://instagram.com">
                                        <i class="fab fa-instagram"></i>
                                    </a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="col-lg-3 col-md-6">
                    <div class="card">
                        <div class="card-body">
                            <img src="img/person3.jpg" alt="" class="img-fluid rounded-circle w-50 mb-3">
                            <h3>John Doe</h3>
                            <h5 class="text-muted">Editors</h5>
                            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eius obcaecati veritatis aut perferendis harum numquam?</p>
                            <div class="d-flex justify-content-center">
                                <div class="p-4">
                                    <a href="http://facebook.com">
                                        <i class="fab fa-facebook"></i>
                                    </a>
                                </div>
                                <div class="p-4">
                                    <a href="http://twitter.com">
                                        <i class="fab fa-twitter"></i>
                                    </a>
                                </div>
                                <div class="p-4">
                                    <a href="http://instagram.com">
                                        <i class="fab fa-instagram"></i>
                                    </a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="col-lg-3 col-md-6">
                    <div class="card">
                        <div class="card-body">
                            <img src="img/person4.jpg" alt="" class="img-fluid rounded-circle w-50 mb-3">
                            <h3>Kevin Swanson</h3>
                            <h5 class="text-muted">Designer</h5>
                            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eius obcaecati veritatis aut perferendis harum numquam?</p>
                            <div class="d-flex justify-content-center">
                                <div class="p-4">
                                    <a href="http://facebook.com">
                                        <i class="fab fa-facebook"></i>
                                    </a>
                                </div>
                                <div class="p-4">
                                    <a href="http://twitter.com">
                                        <i class="fab fa-twitter"></i>
                                    </a>
                                </div>
                                <div class="p-4">
                                    <a href="http://instagram.com">
                                        <i class="fab fa-instagram"></i>
                                    </a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>


CSS:
#authors {
	img {
		margin-top: -50px;    #图像向上移动
	}

	.card:hover {          #hover:当鼠标移到card上的样式：
		background: $primary;  
		color: #fff;
	}
	
	.fab {
		color: #fff;
	}
}
```


## 7. Contact


```html
<section id="contact" class="bg-light py-5">
  			#py-5: padding top and bottom 5px
        <div class="container">
            <div class="row">
                <div class="col-lg-9">
                    <h3>Get In Touch</h3>
                    <p class="lead">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dignissimos, quisquam?</p>
                    <form>
                        <div class="input-group input-group-lg mb-3">
                          #.input-group 类来向表单输入框中添加更多的样式，如图标、文本或者按钮
                          #使用.input-group-prepend 类可以在输入框的的前面添加东西
                          #最后，我们还需要使用 .input-group-text 类来设置文本的样式
                            <div class="input-group-prepend">
                                <span class="input-group-text">
                                    <i class="fas fa-user"></i>
                                </span>
                            </div>
                            <input type="text" class="form-control" placeholder="Name">
                        </div>                    
                    
                    		<div class="input-group input-group-lg mb-3">
                        		<div class="input-group-prepend">
                            		<span class="input-group-text">
                                		<i class="fas fa-envelope"></i>
                            		</span>
                        		</div>
                        		<input type="text" class="form-control" placeholder="Email">
                    		</div>

                    		<div class="input-group input-group-lg mb-3">
                        		<div class="input-group-prepend">
                            		<span class="input-group-text">
                                		<i class="fas fa-pencil-alt"></i>
                            		</span>
                        		</div>
                        		<textarea class="form-control" placeholder="Message" rows="5"></textarea>
                    		</div>

                    		<input type="submit" value="submit" class="btn btn-primary btn-block btn-lg">
                		</form>
            		</div>

            		<div class="col-lg-3 align-self-center">
                		<img src="img/mlogo.png" alt="" class="img-fluid">
                  #img-fluid: 设置响应式图片
            		</div>
        		</div>    
    		</div>
		</section>
```


## 8. Footer

```html
<footer id="main-footer" class="py-5 bg-primary text-white">
     <div class="container">
          <div class="row">
               <div class="col-md-6 ml-auto">
                    <p class="lead">
                        Copyright &copy; 
                        <span id="year"></span>
                    </p>
                </div>
            </div>
     </div>
</footer>


CSS:
<script>
    // Get the current year for the copyright
    $('#year').text(new Date().getFullYear());

    // Init Scrollspy
    $('body').scrollspy({target: '#main-nav'});

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

