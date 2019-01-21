<template>
  <section class="navigation">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-9 navigation">
          <a class="navigation__button" href="#" data-toggle="collapse" data-target="#menu">
            <img class="navigation__button-picture" src="../assets/navButtonCircle.svg">
          </a>

          <ul class="list-unstyled">
            <li class="navigation__main__list">
              <div class="collapse in collapsed__navigation__menu" id="menu">
                <a class="navigation__button" href="#" data-toggle="collapse" data-target="#menu">
                  <img class="navigation__button-picture__inline" src="../assets/navOpen.svg">
                </a>
                <ul class="list-unstyled navigation__list">
                  <li>
                    <a class="navigation__element intro-nav" href="#intro">Introduction</a>
                  </li>
                  <li>
                    <a class="navigation__element types-nav" href="#types">SCS Types</a>
                  </li>
                  <li>
                    <a class="navigation__element behavior-nav" href="#behavior">Behavior</a>
                  </li>
                  <li>
                    <a class="navigation__element usage-nav" href="#dissemination">Usage</a>
                  </li>
                  <li>
                    <a class="navigation__element approval-nav" href="#approval">Approval</a>
                  </li>
                  <li>
                    <a
                      class="navigation__element cityvscountry-nav"
                      href="#cityvscountry"
                    >City / Country</a>
                  </li>
                  <li>
                    <a
                      class="navigation__element perspectives-nav"
                      href="#peoples-perspective"
                    >Perspectives</a>
                  </li>
                  <li>
                    <a class="navigation__element conclusion-nav" href="#conclusion">Conclusion</a>
                  </li>
                </ul>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
$(document).ready(function() {
  var top1 = $("#stage").offset().top - 1;
  var top2 = $("#intro").offset().top - 1;
  var top3 = $("#types").offset().top - 1;
  var top4 = $("#behavior").offset().top - 1;
  var top5 = $("#dissemination").offset().top - 1;
  var top6 = $("#approval").offset().top - 1;
  var top7 = $("#cityvscountry").offset().top - 1;
  var top8 = $("#peoples-perspective").offset().top - 1;
  var top9 = $("#conclusion").offset().top - 1;

  $(document).scroll(function() {
    var scrollPos = $(document).scrollTop();
    if (scrollPos >= top1 && scrollPos < top2) {
      $(".navigation__element").removeClass("nav-active");
    } else if (scrollPos >= top2 && scrollPos < top3) {
      $(".navigation__element").removeClass("nav-active");
      $(".intro-nav").addClass("nav-active");
    } else if (scrollPos >= top3 && scrollPos < top4) {
      $(".navigation__element").removeClass("nav-active");
      $(".types-nav").addClass("nav-active");
    } else if (scrollPos >= top4 && scrollPos < top5) {
      $(".navigation__element").removeClass("nav-active");
      $(".behavior-nav").addClass("nav-active");
    } else if (scrollPos >= top5 && scrollPos < top6) {
      $(".navigation__element").removeClass("nav-active");
      $(".usage-nav").addClass("nav-active");
    } else if (scrollPos >= top6 && scrollPos < top7) {
      $(".navigation__element").removeClass("nav-active");
      $(".approval-nav").addClass("nav-active");
    } else if (scrollPos >= top7 && scrollPos < top8) {
      $(".navigation__element").removeClass("nav-active");
      $(".cityvscountry-nav").addClass("nav-active");
    } else if (scrollPos >= top8 && scrollPos < top9) {
      $(".navigation__element").removeClass("nav-active");
      $(".perspectives-nav").addClass("nav-active");
    } else if (scrollPos >= top9) {
      $(".navigation__element").removeClass("nav-active");
      $(".conclusion-nav").addClass("nav-active");
    }
  });
});

// Stylesheets
import "../style/navigation/navigation.scss";

export default {
  name: "Navigation"
};
</script>
