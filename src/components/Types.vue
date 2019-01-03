<template>
  <section class="types" id="types">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-8 types__intro">
          <h2 class="section__heading">
            <span class="section__heading--light">SCS</span>
            <span class="section__heading--bold">Types</span>
          </h2>
          <p
            class="section__paragraph"
          >To really understand the Social Credit System you should know that there are two types of SCS - commercial and governmental ones.</p>
        </div>
      </div>
      <div class="row justify-content-center types__wrapper">
        <div class="col-6 types__element types__element--commercial-scs">
          <h2 class="types__element__heading">
            <span class="section__heading--bold">Commercial</span>
            <span class="section__heading--light">SCS</span>
          </h2>
          <ul class="types__element__list">
            <li>Eight different SCSs by Chinese companies e. g. Sesame Credit (Alibaba Group) and Tencent Credit</li>
            <li>Free decision of partcipation</li>
          </ul>
          <div class="types__element__approval">
            <h4 class="types__element__subheading">Approval among participants</h4>
            <div class="types__element__approval__bar">
              <div class="types__element__approval__bar-fill"></div>
            </div>
            <div class="types__element__approval__number">55%</div>
          </div>
          <div class="types__element__usage">
            <h4 class="types__element__subheading">Usage</h4>
            <p
              class="types__element__usage__text"
            >4 out of 5 people in China take part in a commercial SCS.</p>

            <div class="types__element__usage__visualization row justify-content-center">
              <div class="col-2 types__element__usage__visualization-element p1"></div>
              <div class="col-2 types__element__usage__visualization-element p2"></div>
              <div class="col-2 types__element__usage__visualization-element p3"></div>
              <div class="col-2 types__element__usage__visualization-element p4"></div>
              <div class="col-2 types__element__usage__visualization-element p5"></div>
            </div>
          </div>
        </div>
        <div class="col-6 types__element types__element--governmental-scs">
          <h2 class="types__element__heading">
            <span class="section__heading--bold">Governmental</span>
            <span class="section__heading--light">SCS</span>
          </h2>
          <ul class="types__element__list">
            <li>40 different SCSs by the government & it’s municipals and provinces</li>
            <li>Some model cities with more strongly developed SCS e. g. Rongcheng and Weihai</li>
            <li>Mandatory participation</li>
          </ul>
          <div class="types__element__approval">
            <h4 class="types__element__subheading">Approval among participants</h4>
            <div class="types__element__approval__bar">
              <div class="types__element__approval__bar-fill"></div>
            </div>
            <div class="types__element__approval__number">64%</div>
          </div>
          <div class="types__element__usage">
            <h4 class="types__element__subheading">Usage</h4>
            <p
              class="types__element__usage__text"
            >Approximately 2 out of 5 people in China take part in a governmental SCS.</p>

            <div class="types__element__usage__visualization row justify-content-center">
              <div class="col-2 types__element__usage__visualization-element p1"></div>
              <div class="col-2 types__element__usage__visualization-element p2"></div>
              <div class="col-2 types__element__usage__visualization-element p3"></div>
              <div class="col-2 types__element__usage__visualization-element p4"></div>
              <div class="col-2 types__element__usage__visualization-element p5"></div>
            </div>

            <p
              class="types__element__usage__text"
            >Only 11% of these affected citizens know that they take part.</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
// Stylesheets
import "../style/types/types.scss";

export default {
  name: "Types"
};
</script>