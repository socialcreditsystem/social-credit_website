<template>
  <section class="peoples-perspective wow fadeIn" data-wow-duration="2s" id="peoples-perspective">
    <div class="container">
      <div class="row justify-content-center peoples-perspective__intro">
        <div class="col-6">
          <h2 class="section__heading">
            <span class="section__heading--bold">People's</span>
            <span class="section__heading--light">&nbsp;Perspective</span>
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
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--1.jpg">
          </td>
        </tr>
        <tr>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--2.jpg">
          </td>
          <td colspan="6"></td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--3.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--4.jpg">
          </td>
        </tr>
        <tr>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--5.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--6.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--7.jpg">
          </td>
          <td v-on:click="changeToPerson(0)" class="peoples-perspective__table--clickable">
            <img src="../assets/imgs/PeoplesPerspective/Clickable/people-clickable-1.jpg">
          </td>
          <td v-on:click="changeToPerson(1)" class="peoples-perspective__table--clickable">
            <img src="../assets/imgs/PeoplesPerspective/Clickable/people-clickable-2.jpg">
          </td>
          <td v-on:click="changeToPerson(2)" class="peoples-perspective__table--clickable">
            <img src="../assets/imgs/PeoplesPerspective/Clickable/people-clickable-3.jpg">
          </td>
          <td v-on:click="changeToPerson(3)" class="peoples-perspective__table--clickable">
            <img src="../assets/imgs/PeoplesPerspective/Clickable/people-clickable-4.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--8.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--9.jpg">
          </td>
        </tr>
        <tr>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--10.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--11.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--12.jpg">
          </td>
          <td v-on:click="changeToPerson(4)" class="peoples-perspective__table--clickable">
            <div class="peoples-perspective__table--clickable__interview-info" id="interviewInfo">
              <p class="peoples-perspective__table--clickable__interview-info--interview-date">June 2018</p>
              <p class="peoples-perspective__table--clickable__interview-info--interview-number">Interview 10</p>
              </div>
            <img src="../assets/imgs/PeoplesPerspective/Clickable/people-clickable-5.jpg">
          </td>
          <td colspan="4" rowspan="4" class="peoples-perspective__table__content">
            <p class="peoples-perspective__table__content__paragraph" id="quoteContent">
              „Take, for instance, the example of using shared bikes.
              If someone does not lock a shared bike after using it properly, her or his own credit will be influenced. Alipay can collect such very detailed information from different aspects in life and include this in a score. Through such detailed accounting, SCS can track individuals’ actions and create trust in society“
            </p>
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--13.jpg">
          </td>
        </tr>
        <tr>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--14.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--15.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--16.jpg">
          </td>
          <td v-on:click="changeToPerson(5)" class="peoples-perspective__table--clickable">
            <img src="../assets/imgs/PeoplesPerspective/Clickable/people-clickable-6.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--17.jpg">
          </td>
        </tr>
        <tr>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--18.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--19.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--20.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--21.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--22.jpg">
          </td>
        </tr>
        <tr>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--1.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--2.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--3.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--4.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--5.jpg">
          </td>
        </tr>
        <tr>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--6.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--7.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--8.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--9.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--10.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--11.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--12.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--13.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--14.jpg">
          </td>
        </tr>
        <tr class="peoples-perspective__table--last-row">
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--15.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--16.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--17.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--18.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--19.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--20.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--21.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--22.jpg">
          </td>
          <td>
            <img src="../assets/imgs/PeoplesPerspective/NotClickable/people--1.jpg">
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
  "Interview 5",
  "June 2018",
  "Sometimes there is not enough money left in Alipay and Sesame Credit can be used for ordering delivery food.This is convenient and increases life quality."
];
let person2 = [
  "Interview 9",
  "July 2018",
  "[...] generate a guide and norm for personal social behavior with the Chinese society. It could improve the efficiency of social operations."
];
let person3 = [
  "Interview 5",
  "June 2018",
  "SCS can create trust in society through feedback mechanisms. People with bad credit will be less likely to be employed and it will not be easy for them to access more funds in the future. Such punishments provide feedback to people with bad behaviour to restrain themselves. Step by step, SCSs will create trust in society."
];
let person4 = [
  "Interview 7",
  "June 2018",
  "All data is accessible to the CCP already. For instance, during the registration for primary school, people must provide detailed family information. So I do not think that there is any point in worrying about the Party having access to data through the SCS, because it is inevitable that all data is accessible to CCP."
];
let person5 = [
  "Interview 10",
  "June 2018",
  "Take, for instance, the example of using shared bikes. If someone does not lock a shared bike after using it properly, her or his own credit will be influenced. Alipay can collect such very detailed information from different aspects in life and include this in a score. Through such detailed accounting, SCSs can track individuals’ actions and create trust in society."
];
let person6 = [
  "Interview 8",
  "June 2018",
  "The collection of private personal data depends on the consciousness and governance of the Party. If personal data is used for good reasons, I think it is acceptable."
];
let persons = [person1, person2, person3, person4, person5, person6];

export default {
  name: "PeoplesPerspective",
  methods: {
    changeToPerson(person) {
      let cellHTML = event.target.parentNode.innerHTML;
      let newDivClass = "peoples-perspective__table--clickable__interview-info";
      if (
        !cellHTML.includes(newDivClass) &&
        event.target.parentNode.className ==
          "peoples-perspective__table--clickable"
      ) {
        let currentPerson = persons[person];

        document.getElementById("quoteContent").innerText =
          '"' + currentPerson[2] + '"';

        let oldElement = document.getElementById("interviewInfo");

        if (oldElement) {
          oldElement.parentNode.removeChild(oldElement);
        }

        let newDiv = document.createElement("div");
        newDiv.setAttribute("class", newDivClass);
        newDiv.id = "interviewInfo";
        let interviewDate = document.createElement("p");
        interviewDate.setAttribute(
          "class",
          "peoples-perspective__table--clickable__interview-info--interview-date"
        );
        interviewDate.appendChild(document.createTextNode(currentPerson[1]));
        let interviewNumber = document.createElement("p");
        interviewNumber.setAttribute(
          "class",
          "peoples-perspective__table--clickable__interview-info--interview-number"
        );
        interviewNumber.appendChild(document.createTextNode(currentPerson[0]));
        newDiv.appendChild(interviewDate);
        newDiv.appendChild(interviewNumber);

        let element = event.target.parentNode;
        element.insertBefore(newDiv, event.target);
      }
    }
  }
};
</script>