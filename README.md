# my-cv
this is for hosting
<!DOCTYPE html>
<html>
<?php
$connection = mysqli_connect('localhost', 'root', '', 'portfolio');
?>

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1">
    <link rel="shortcut icon" href="assets/images/logo-58x58.png" type="image/x-icon">
    <meta name="description" content="">

    <title>Home</title>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Raleway:400,100,200,300,500,600,700,800,900">
    <link rel="stylesheet" href="assets/bootstrap/css/bootstrap.min.css">
    <link rel="stylesheet" href="assets/socicon/css/socicon.min.css">
    <link rel="stylesheet" href="assets/font-awesome/css/font-awesome.min.css">
    <link rel="stylesheet" href="assets/slick/slick.css">
    <link rel="stylesheet" href="assets/unicore/css/style.css">
    <link rel="stylesheet" href="assets/dropdown-menu/style.light.css">
    <link rel="stylesheet" href="assets/mobirise-slider/style.css">
    <link rel="stylesheet" href="assets/mobirise/css/mbr-additional.css" type="text/css">
</head>

<body>
    <section id="dropdown-menu1-5" data-rv-view="78">

        <nav class="navbar navbar-dropdown mbr-title-font navbar-fixed-top">

            <div class="container">

                <div class="navbar-brand">
                    <a href="" class="navbar-logo"><img src="assets/images/logo-58x58.png" alt="Nisarg"></a>
                    <a class="text-black" href=""></a>
                </div>

                <button class="navbar-toggler pull-xs-right hidden-md-up" type="button" data-toggle="collapse" data-target="#exCollapsingNavbar">
                    ☰
                </button>

                <ul class="nav-dropdown collapse pull-xs-right navbar-toggleable-sm nav navbar-nav" id="exCollapsingNavbar">
                    <?php $query = "SELECT * FROM header_menus WHERE `status`=1";
                    $result = mysqli_query($connection, $query);
                    while ($row = mysqli_fetch_array($result)) {
                        echo '
                        <li class="nav-item nav-btn"><a class="nav-link btn mbr-title-font btn-info" href="' . $row['link'] . '" >' . $row['title'] . '</a></li>
        ';
                    } ?>
                </ul>

            </div>

        </nav>

    </section>

    <?php 
    $query = "SELECT * FROM header_content WHERE `status`=1";
    $result = mysqli_query($connection, $query);
    while ($row = mysqli_fetch_array($result)) { ?>
    <section class="mbr-section--bg-adapted mbr-after-navbar" id="header7-o" data-rv-view="265" style="background-image: url(<?php echo 'data:image/jpeg;base64,' . base64_encode($row["image"]) ?>);">
        <div class="intro intro14" style="padding-top: 270px; padding-bottom: 230px;">
            <div class="mbr-overlay" style="opacity: 0.7; background-color: rgb(21, 21, 21);"></div>
            <div class="container">
                <div class="row center-content">
                    <div class="col-md-10 col-md-offset-1 text-center">
                        <h3 class="mbr-title-font"> <?php echo $row["head_line"]; ?></h3>
                        <p><?php echo $row["description"]; ?></p>
                        <div class="space40"></div>
                        <div><a href="<?php echo $row["linkedin"]; ?>" class="btn mbr-title-font btn-lg btn-primary" target="_blank">Join me On Linkedin</a>
                            <a href="<?php echo $row["github"]; ?>" class="btn mbr-title-font btn-lg btn-primary" target="_blank">Explore Me On Github</a></div>

                        <ul class="features-list">
                            <li>
                                <i class="fa fa-database"></i>
                                <h5 class="mbr-title-font">Project Handling</h5>
                            </li>

                            <li>
                                <i class="fa fa-lightbulb-o"></i>
                                <h5 class="mbr-title-font">Creative Thinking</h5>
                            </li>

                            <li>
                                <i class="fa fa-money"></i>
                                <h5 class="mbr-title-font">Marketing Skills</h5>
                            </li>

                            <li>
                                <i class="fa fa-book"></i>
                                <h5 class="mbr-title-font">Reader</h5>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <?php 
    break;
}
?>

    <section class="mbr-section--bg-adapted mbr-section--relative" id="msg-box4-b" data-rv-view="103" style="background-color: rgb(255, 255, 255);">
        <div class="elements-content" style="padding-top: 100px; padding-bottom: 100px;">

            <div class="container">
                <div class="section-head text-center space10">
                    <h1 class="mbr-title-font" id=aboutme>About Me</h1>
                    <hr>
                </div>
                <div class="row">
                    <div class="col-md-12">
                        <div class="row center-content">
                            <?php
                            $query = "SELECT * FROM home_about WHERE `status`=1";
                            $result = mysqli_query($connection, $query);
                            while ($row = mysqli_fetch_array($result)) {
                                ?>
                            <div class="col-md-5">
                                <h3 class="text-uppercase space20 mbr-title-font"><strong><?php echo $row['tag_line']; ?></strong></h3>
                                <p><?php echo $row['description']; ?></p>
                                <div class="space30"></div>
                                <div><a class="btn mbr-title-font btn-primary" href="<?php echo $row['about_link']; ?>" target="_blank">Know More About me</a></div>
                            </div>
                            <div class="col-md-7">
                                <figure class="mbr-figure mbr-figure--adapted mbr-figure--caption-inside-bottom mbr-figure--full-width">
                                    <img src="<?php echo 'data:image/jpeg;base64,' . base64_encode($row['image']); ?>" class="mbr-figure__img"></figure>
                            </div>
                            <?php 
                            break;
                        }
                        ?>
                        </div>
                    </div>
                </div>
            </div>
        </div>

    </section>

    <section class="mbr-section--bg-adapted mbr-section--relative" id="progressBar-7" data-rv-view="82" style="background-color: rgb(255, 255, 255);">

        <div class="elements-content" style="padding-top: 50px; padding-bottom: 5px;">
            <div class="container">
                <div class="row">
                    <div class="col-md-10 col-md-offset-1">
                        <div class="section-head text-center space10">
                            <h1 class="mbr-title-font" id=myskills>My Skills</h1>
                            <br>
                        </div>
                        <div class="clearfix"></div>

                        <div class="progress">
                            <h5 class="mbr-title-font">Leadership</h5>
                            <div class="progress-bar progress-bar-success mbr-primary-bgColor" role="progressbar" aria-valuemin="0" aria-valuemax="100" aria-valuenow="75%" style="width:75%">75%</div>
                        </div>
                        <div class="progress">
                            <h5 class="mbr-title-font">Marketing</h5>
                            <div class="progress-bar progress-bar-info" role="progressbar" aria-valuenow="value2" aria-valuemin="0" aria-valuemax="100" style="width:88%">88%</div>
                        </div>
                        <div class="progress">
                            <h5 class="mbr-title-font">Speaking</h5>
                            <div class="progress-bar progress-bar-warning" role="progressbar" aria-valuenow="value3" aria-valuemin="0" aria-valuemax="100" style="width:96%">96%</div>
                        </div>
                        <div class="progress">
                            <h5 class="mbr-title-font">Project Mangment</h5>
                            <div class="progress-bar progress-bar-danger" role="progressbar" aria-valuenow="value4" aria-valuemin="0" aria-valuemax="100" style="width:80%">80%</div>
                        </div>

                        <div class="progress">
                            <h5 class="mbr-title-font">Business Intelligence</h5>
                            <div class="progress-bar progress-bar-success mbr-primary-bgColor" role="progressbar" aria-valuemin="0" aria-valuemax="100" aria-valuenow="58%" style="width:58%">58%</div>
                        </div>
                        <div class="progress">
                            <h5 class="mbr-title-font">Content Idea Strategy</h5>
                            <div class="progress-bar progress-bar-info" role="progressbar" aria-valuenow="value6" aria-valuemin="0" aria-valuemax="100" style="width:48%">48%</div>
                        </div>


                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="services icon-box services mbr-section--bg-adapted mbr-section--relative" id="features4-l" data-rv-view="200" style="background-color: rgb(255, 255, 255); padding-top: 100px; padding-bottom: 100px;">
        <div class="section-head text-center ">
            <h1 class="mbr-title-font">Education</h1>
            <br>
            <br>
            <br>
            <span class=space10></span>
        </div>
        <div class="container">
            <div class="row">
                <?php 
                $query = "SELECT * FROM home_education WHERE `status`=1";
                $result = mysqli_query($connection, $query);
                echo '<ul>';
                while ($row = mysqli_fetch_array($result)) {
                    echo '<div class="col-md-4 col-sm-4">
                    <div class="service-box">
                        <i class="fa mbr-primary-color fa-book"></i>
                        <div>
                            <h4 class="mbr-title-font">' . $row['course'] . '</h4>
                            <p>' . $row['details'] . '
                                <br><br></p>
                        </div>
                    </div>
                </div>';
                } ?>
            </div>
        </div>
    </section>

    <section class="mbr-slider mbr-section mbr-section--no-padding carousel slide" data-ride="carousel" data-wrap="true" data-interval="5000" id="slider2-8" data-rv-view="85" style="background-color: rgb(255, 255, 255);">
        <div class="section-head text-center space10">
            <h1 class="mbr-title-font" id="mytalk">My Talks</h1>
            <br>
            <br>
            <br>
            <br>
        </div>
        <div class="mbr-section__container">
            <div>
                <ol class="carousel-indicators">
                    <li data-app-prevent-settings="" data-target="#slider2-8" data-slide-to="0" class="active"></li>
                    <li data-app-prevent-settings="" data-target="#slider2-8" class="" data-slide-to="1"></li>
                    <li data-app-prevent-settings="" data-target="#slider2-8" data-slide-to="2"></li>
                </ol>
                <div class="carousel-inner" role="listbox">
                    <?php 

                    $query = "SELECT * FROM my_talks WHERE `status`=1";
                    $result = mysqli_query($connection, $query);
                    $i = 1;
                    while ($row = mysqli_fetch_array($result)) {
                        if ($i == 1) { ?>

                    <div class="mbr-box mbr-section mbr-section--relative mbr-section--fixed-size mbr-section--bg-adapted item dark center mbr-section--full-height active" style="background-image: url(<?php echo 'data:image/jpeg;base64,' . base64_encode($row['image']); ?>);">
                        <div class="mbr-box__magnet mbr-box__magnet--center-left mbr-box__magnet--sm-padding">

                            <div class=" container">

                                <div class="row">
                                    <div class=" col-md-offset-1 col-md-6">

                                        <div class="mbr-hero">
                                            <h1 class="mbr-hero__text mbr-title-font"><?php echo $row['description'];
                                                                                        $i++; ?></h1>

                                        </div>

                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <?php 
                } else if ($i == 2) { ?>
                    <div class="mbr-box mbr-section mbr-section--relative mbr-section--fixed-size mbr-section--bg-adapted item dark center mbr-section--full-height" style="background-image: url(<?php echo 'data:image/jpeg;base64,' . base64_encode($row['image']); ?>);">
                        <div class="mbr-box__magnet mbr-box__magnet--center-left mbr-box__magnet--sm-padding">

                            <div class=" container">

                                <div class="row">
                                    <div class=" col-md-offset-1 col-md-6">

                                        <div class="mbr-hero">
                                            <h1 class="mbr-hero__text mbr-title-font"><?php echo $row['description'];
                                                                                        $i++; ?></h1>


                                        </div>

                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <?php 
                } else { ?>
                    <div class="mbr-box mbr-section mbr-section--relative mbr-section--fixed-size mbr-section--bg-adapted item dark center mbr-section--full-height" style="background-image: url(<?php echo 'data:image/jpeg;base64,' . base64_encode($row['image']); ?>);">
                        <div class="mbr-box__magnet mbr-box__magnet--center-left mbr-box__magnet--sm-padding">

                            <div class=" container">

                                <div class="row">
                                    <div class=" col-md-offset-1 col-md-6">

                                        <div class="mbr-hero">
                                            <h1 class="mbr-hero__text mbr-title-font"><?php echo $row['description'];
                                                                                        $i++; ?></h1>


                                        </div>

                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <?php 
            }
        } ?>
                <a data-app-prevent-settings="" class="left carousel-control" role="button" data-slide="prev" href="#slider2-8">
                    <span class="glyphicon glyphicon-menu-left" aria-hidden="true"></span>
                    <span class="sr-only">Previous</span>
                </a>
                <a data-app-prevent-settings="" class="right carousel-control" role="button" data-slide="next" href="#slider2-8">
                    <span class="glyphicon glyphicon-menu-right" aria-hidden="true"></span>
                    <span class="sr-only">Next</span>
                </a>
            </div>
        </div>
    </section>
    <br>
    <br>
    <br>
    <br>
    <br>

    <section class="mbr-slider mbr-section mbr-section--no-padding carousel slide" data-ride="carousel" data-wrap="true" data-interval="5000" id="slider2-n" data-rv-view="241" style="background-color: rgb(255, 255, 255);">
        <div class="section-head text-center ">
            <h1 class="mbr-title-font" id="achivement">Achivement</h1>
        </div>
        <div class="mbr-section__container boxed-slider container" style="padding-top: 93px; padding-bottom: 93px;">
            <div>
                <ol class="carousel-indicators">
                    <li data-app-prevent-settings="" data-target="#slider2-n" data-slide-to="0" class="active"></li>
                    <li data-app-prevent-settings="" data-target="#slider2-n" data-slide-to="1"></li>
                    <li data-app-prevent-settings="" data-target="#slider2-n" class="" data-slide-to="2"></li>
                </ol>
                <div class="carousel-inner" role="listbox">
                    <?php
                    $query = "SELECT * FROM my_achivements WHERE `status`=1";
                    $result = mysqli_query($connection, $query);
                    $i = 1;
                    while ($row = mysqli_fetch_array($result)) {
                        if ($i == 1) { ?>
                    <div class="mbr-box mbr-section mbr-section--relative mbr-section--fixed-size mbr-section--bg-adapted item dark center active">
                        <div class="mbr-box__magnet mbr-box__magnet--center-left">
                            <div class="mbr-overlay"></div>
                            <div>
                                <img src="<?php echo 'data:image/jpeg;base64,' . base64_encode($row['image']); ?>">
                                <div class="row">
                                    <div class=" col-md-offset-1 col-md-6">

                                        <div class="mbr-hero">
                                            <h1 class="mbr-hero__text mbr-title-font"><?php echo $row['title'];
                                                                                        $i++; ?></h1>


                                        </div>

                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <?php 
                } else if ($i == 2) { ?>
                    <div class="mbr-box mbr-section mbr-section--relative mbr-section--fixed-size mbr-section--bg-adapted item dark center">
                        <div class="mbr-box__magnet mbr-box__magnet--center-left">
                            <div class="mbr-overlay"></div>
                            <div>
                                <img src="<?php echo 'data:image/jpeg;base64,' . base64_encode($row['image']); ?>">
                                <div class="row">
                                    <div class=" col-md-offset-1 col-md-6">

                                        <div class="mbr-hero">
                                            <h1 class="mbr-hero__text mbr-title-font"><?php echo $row['title']; ?></h1>


                                        </div>

                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <?php 
                } else { ?>
                    <div class="mbr-box mbr-section mbr-section--relative mbr-section--fixed-size mbr-section--bg-adapted item dark center">
                        <div class="mbr-box__magnet mbr-box__magnet--center-left">
                            <div class="mbr-overlay"></div>
                            <div>
                                <img src="<?php echo 'data:image/jpeg;base64,' . base64_encode($row['image']); ?>">
                                <div class="row">
                                    <div class=" col-md-offset-1 col-md-6">

                                        <div class="mbr-hero">
                                            <h1 class="mbr-hero__text mbr-title-font"><?php echo $row['title']; ?></h1>


                                        </div>

                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div> <?php 
                    }
                } ?>

                <a data-app-prevent-settings="" class="left carousel-control" role="button" data-slide="prev" href="#slider2-n">
                    <span class="glyphicon glyphicon-menu-left" aria-hidden="true"></span>
                    <span class="sr-only">Previous</span>
                </a>
                <a data-app-prevent-settings="" class="right carousel-control" role="button" data-slide="next" href="#slider2-n">
                    <span class="glyphicon glyphicon-menu-right" aria-hidden="true"></span>
                    <span class="sr-only">Next</span>
                </a>
            </div>
        </div>
    </section>

    <section class="mbr-section--bg-adapted mbr-section--relative" id="testimonials3-i" data-rv-view="162" style="background-color: rgb(255, 255, 255);">
        <div class="testimonials3 testimonials testimonials-white" style="padding-top: 40px; padding-bottom: 140px;">

            <div class="container">
                <div class="section-head text-center col-md-8 col-md-offset-2 space50">
                    <h1 class="mbr-title-font" id="testimonials">TESTIMONIALS</h1>
                </div>
                <div class="row">
                    <div class="col-md-12 text-center">
                        <div class="quote3 testimonials3-i">
                            <?php $query = "SELECT * FROM testimonials WHERE `status`=1";
                            $result = mysqli_query($connection, $query);
                            while ($row = mysqli_fetch_array($result)) { ?>
                            <div>
                                <p><?php echo $row['description']; ?></p>
                                <figure class="mbr-figure mbr-figure--adapted mbr-figure--full-width"><img src="<?php echo 'data:image/jpeg;base64,' . base64_encode($row['image']); ?>" class="mbr-figure__img"></figure>
                                <span class="author"><?php echo $row['name'] . ' - ' . $row['position_company']; ?></span>
                            </div>
                            <?php 
                        } ?>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <hr>

    <section class="mbr-section mbr-section--relative mbr-section--fixed-size" id="social-buttons2-f" data-rv-view="147" style="background-color: rgb(255, 255, 255);">
        <div class="mbr-section__container container">
            <div class="mbr-header mbr-header--inline row" style="padding-top: 40.8px; padding-bottom: 40.8px;">
                <div class="col-sm-4">
                    <h3 class="mbr-header__text mbr-title-font">FOLLOW US</h3>
                </div>
                <div class="mbr-social-icons mbr-social-icons--style-1 col-sm-8"><a class="mbr-social-icons__icon socicon-bg-twitter" title="Twitter" target="_blank" href="https://relationtechnonisnanu.blogspot.com/"><i class="socicon socicon-twitter"></i></a> <a class="mbr-social-icons__icon socicon-bg-facebook" title="Facebook" target="_blank" href="https://stackoverflow.com/users/9667616/nisarg-mehta"><i class="socicon socicon-facebook"></i></a> <a class="mbr-social-icons__icon socicon-bg-instagram" title="Instagram" target="_blank" href="https://www.instagram.com/geniuspersonalitynisargmehta/?hl=en"><i class="socicon socicon-instagram"></i></a> <a class="mbr-social-icons__icon socicon-bg-github" title="GitHub" target="_blank" href="https://github.com/nisargmehtanm"><i class="socicon socicon-github"></i></a> <a class="mbr-social-icons__icon socicon-bg-linkedin" title="LinkedIn" target="_blank" href="https://www.linkedin.com/in/nisarg-mehta-202a4b106/?locale=hi_IN"><i class="socicon socicon-linkedin"></i></a> </div>
            </div>
        </div>
    </section>

    <hr>

    <section class="mbr-section--bg-adapted mbr-section--relative" id="contacts4-t" data-rv-view="280" style="background-color: rgb(255, 255, 255);">
        <footer class="footer2" id="footer2" style="padding-top: 80px; padding-bottom: 60px;">

            <div class="container">
                <div class="row">
                    <?php $query = "SELECT * FROM footer WHERE `status`=1";
                    $result = mysqli_query($connection, $query);

                    while ($row = mysqli_fetch_array($result)) {
                        echo '<div class="col-md-4">
                        <h1 class="footer-logo mbr-title-font">Address</h1>
                        <p>' . $row['street'] . ', ' . $row['city'] . ' - ' . $row['zipcode'] . ', ' . $row['state'] . ', ' . $row['country'] . '
                        <br><br>Email :' . $row['email'] . '<br><br>Phone :&nbsp;' . $row['phone'] . '<br><br></p>
                        <p></p>
                    </div>';
                        break;
                    } ?>

                    <div class="col-md-4" data-form-type="formoid">
                        <h5 class="mbr-title-font">Quick Message</h5>

                        <div data-form-alert="true">
                            <div class="hide" data-form-alert-success="true">Thanks for filling out form!</div>
                        </div>
                        <form id="contactForm" class="positioned" action="https://mobirise.com/" method="post" data-form-title="Quick Message">
                            <input type="hidden" value="KFB0hKABElO/OOYvNEgMUInadmfNiajTprGHhutFwY/lWX71ApRYrTZlsmbPyUN+44mRrpkAC2J325Tu51xVw6Hi/lLNOTt1aEWDNdXS5yzhodRg0NU8LUbmh+dFJHLt" data-form-email="true">
                            <div>
                                <input type="text" class="form-control" name="name" required="" placeholder="Your Name here" data-form-field="Name">
                            </div>
                            <div>
                                <input type="email" class="form-control" name="email" required="" placeholder="Email Address here" data-form-field="Email">
                            </div>
                            <textarea class="form-control" name="message" rows="4" placeholder="Message here" data-form-field="Message"></textarea>
                            <div><button type="submit" class="btn mbr-title-font btn-ico btn-info">Send Message<i class="fa fa-paper-plane-o"></i></button></div>
                        </form>

                    </div>

                    <div class="col-md-4">
                        <!-- GOOGLE MAP -->
                        <div class="google-map">
                            <div class="container-fluid no-padding">
                                <figure class="mbr-figure mbr-figure--wysiwyg mbr-figure--full-width mbr-figure--no-bg">
                                    <div class="mbr-figure__map" style="height: 278px"><iframe frameborder="0" style="border:0" src="https://www.google.com/maps/embed/v1/place?key=AIzaSyCy9r70T3NYf3PhvVflTo0_zdif2_IoIYs&amp;q=place_id:ChIJPXRO5H_JWTkRGGraeo0Llog" allowfullscreen=""></iframe></div>
                                </figure>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </footer>
    </section>

    <section class="mbr-section--bg-adapted mbr-section--relative" id="footer1-u" data-rv-view="289" style="background-color: rgb(17, 17, 17);">
        <div class="footer-copy" style="padding-top: 20px; padding-bottom: 20px;">

            <div class="container mbr-title-font">© 2019. Design and Develop By Nisarg Mheta</div>
        </div>
    </section>


    <script src="assets/web/assets/jquery/jquery.min.js"></script>
    <script src="assets/bootstrap/js/bootstrap.min.js"></script>
    <script src="assets/smooth-scroll/SmoothScroll.js"></script>
    <script src="assets/slick/slick.js"></script>
    <script src="assets/bootstrap-carousel-swipe/bootstrap-carousel-swipe.js"></script>
    <script src="assets/unicore/js/script.js"></script>
    <script src="assets/dropdown-menu/script.js"></script>
    <script src="assets/formoid/formoid.min.js"></script>


</body>

</html> 
