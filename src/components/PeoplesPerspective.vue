<template>
  <section class="peoples-perspective wow fadeIn" data-wow-duration="2s" id="peoples-perspective">
    <div class="container">
      <div class="row justify-content-center peoples-perspective__intro">
        <div class="col-6">
          <h2 class="section__heading">
            <span class="section__heading--bold">People's</span>
            <span class="section__heading--light">Perspective</span>
          </h2>
          <p
            class="section__paragraph"
          >We have already seen that the Chinese are very positive about the SCS. The best way to understand why this is the case is to let the citizens speak.</p>
        </div>
      </div>
    </div>
    <table class="peoples-perspective__table">
      <div class="peoples-perspective__overlay peoples-perspective__overlay--horizontal"></div>
      <div class="peoples-perspective__overlay peoples-perspective__overlay--vertical"></div>
      <tbody>
        <tr>
          <td colspan="8"></td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
        </tr>
        <tr>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td colspan="6"></td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
        </tr>
        <tr>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td v-on:click="changeToPerson(1)" class="peoples-perspective__table--clickable">
            <img src="https://picsum.photos/300/300">
          </td>
          <td v-on:click="changeToPerson(0)" class="peoples-perspective__table--clickable">
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
        </tr>
        <tr>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td colspan="4" rowspan="4" class="peoples-perspective__table__content">
            <p class="peoples-perspective__table__content__paragraph" id="quoteContent">
              „Take, for instance, the example of using shared bikes.
              If someone does not lock a shared bike after using it properly, her or his own credit will be influenced. Alipay can collect such very detailed information from different aspects in life and include this in a score. Through such detailed accounting, SCSs can track individuals’ actions and create trust in society“
            </p>
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
        </tr>
        <tr>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
        </tr>
        <tr>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
        </tr>
        <tr>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
        </tr>
        <tr>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
        </tr>
        <tr class="peoples-perspective__table--last-row">
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
          <td>
            <img src="https://picsum.photos/300/300">
          </td>
        </tr>
      </tbody>
    </table>
  </section>
</template>

<script>
// Stylesheets
import "../style/peoples-perspective/peoples-perspective.scss";

let person1 = [
  "Interview 5, June 2018",
  "sometimes there is not enough money left in Alipay and Sesame Credit can be used for ordering delivery food.\nThis is convenient and increases life quality."
];
let person2 = [
  "Interview 9, July 2018",
  "generate a guide and norm for personal social behavior with the Chinese society. It could improve the efficiency of social operations"
];
let persons = [person1, person2];

export default {
  name: "PeoplesPerspective",
  methods: {
    changeToPerson(person) {
      let cellHTML = event.target.parentNode.innerHTML;
      let newDivClass = "peoples-perspective__table--clickable__interview-info";

      if (!cellHTML.includes(newDivClass)) {
        let currentPerson = persons[person];

        document.getElementById("quoteContent").innerText =
          '"' + currentPerson[1] + '"';

        let oldElement = document.getElementById("interviewInfo");

        if (oldElement) {
          oldElement.parentNode.removeChild(oldElement);
        }

        let newDiv = document.createElement("div");
        newDiv.setAttribute("class", newDivClass);
        newDiv.id = "interviewInfo";
        let node = document.createTextNode(currentPerson[0]);
        newDiv.appendChild(node);

        let element = event.target.parentNode;
        element.insertBefore(newDiv, event.target);
      }
    }
  }
};
</script>