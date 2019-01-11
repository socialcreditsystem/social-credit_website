<template>
  <section class="navigation">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-9 navigation">
          <ul class="list-unstyled">
            <li>
              <a class="navigation_button" href="#" data-toggle="collapse" data-target="#Menu">
                <img class="navigation-button-picture" src="../assets/navigation-plus.svg">
              </a>
              <div class="collapse in" id="Menu">
                <div class="triangle"></div>
                <ul class="list-unstyled navigation_list">
                  <a class="navigation_element intro-nav" href="#intro">Introduction</a>

                  <li>
                    <a class="navigation_element types-nav" href="#types">SCS-Types</a>
                  </li>
                  <li>
                    <a class="navigation_element behavior-nav" href="#behavior">Behavior</a>
                  </li>
                  <li>
                    <a class="navigation_element usage-nav" href="#dissemination">Usage</a>
                  </li>
                  <li>
                    <a class="navigation_element approval-nav" href="#approval">Approval</a>
                  </li>
                  <li>
                    <a
                      class="navigation_element cityvscountry-nav"
                      href="#cityvscountry"
                    >City vs. Country</a>
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

  $(document).scroll(function() {
    var scrollPos = $(document).scrollTop();
    if (scrollPos >= top1 && scrollPos < top2) {
      $(".navigation_element").removeClass("nav-active");
    } else if (scrollPos >= top2 && scrollPos < top3) {
      $(".navigation_element").removeClass("nav-active");
      $(".intro-nav").addClass("nav-active");
    } else if (scrollPos >= top3 && scrollPos < top4) {
      $(".navigation_element").removeClass("nav-active");
      $(".types-nav").addClass("nav-active");
    } else if (scrollPos >= top4 && scrollPos < top5) {
      $(".navigation_element").removeClass("nav-active");
      $(".behavior-nav").addClass("nav-active");
    } else if (scrollPos >= top5 && scrollPos < top6) {
      $(".navigation_element").removeClass("nav-active");
      $(".usage-nav").addClass("nav-active");
    } else if (scrollPos >= top6 && scrollPos < top7) {
      $(".navigation_element").removeClass("nav-active");
      $(".approval-nav").addClass("nav-active");
    } else if (scrollPos >= top7) {
      $(".navigation_element").removeClass("nav-active");
      $(".cityvscountry-nav").addClass("nav-active");
    }
  });
});

// Stylesheets
import "../style/navigation/navigation.scss";

export default {
  name: "Navigation"
};
</script>
