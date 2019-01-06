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
                  <li class="active">
                    <a class="navigation_element intro-nav" href="#intro">Introduction</a>
                  </li>
                  <li>
                    <a class="navigation_element behavior-nav" href="#behavior">Behavior</a>
                  </li>
                  <li>
                    <a class="navigation_element types-nav" href="#types">SCS-Types</a>
                  </li>
                  <li>
                    <a class="navigation_element usage-nav" href="#usage">Usage</a>
                  </li>
                  <li>
                    <a class="navigation_element approval-nav" href="#approval">
                      <i class="glyphicon glyphicon-user"></i> Approval
                    </a>
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
  var top1 = $("#stage").offset().top;
  var top2 = $("#intro").offset().top;
  var top3 = $("#types").offset().top;

  $(document).scroll(function() {
    var scrollPos = $(document).scrollTop();
    if (scrollPos >= top1 && scrollPos < top2) {
      $(".navigation_element").removeClass("nav-active");
      $(".stage-nav").addClass("nav-active");
    } else if (scrollPos >= top2 && scrollPos < top3) {
      $(".navigation_element").removeClass("nav-active");
      $(".intro-nav").addClass("nav-active");
    } else if (scrollPos >= top3) {
      $(".navigation_element").removeClass("nav-active");
      $(".types-nav").addClass("nav-active");
    }
  });
});

// Stylesheets
import "../style/navigation/navigation.scss";

export default {
  name: "Navigation"
};
</script>
