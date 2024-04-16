# toggle-button-using-CSS
* {
  user-select: none;
  -webkit-tap-highlight-color: transparent;
}

*:focus {
  outline: none;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  margin: 0;
  background-color: #f1f9f9;
}

#app-cover {
  display: table;
  width: 600px;
  margin: 80px auto;
  counter-reset: button-counter;
}

.row {
  display: table-row;
}

.toggle-button-cover {
  display: table-cell;
  position: relative;
  width: 200px;
  height: 140px;
  box-sizing: border-box;
}

.button-cover {
  height: 100px;
  margin: 20px;
  background-color: #fff;
  box-shadow: 0 10px 20px -8px #c5d6d6;
  border-radius: 4px;
}

.button-cover:before {
  counter-increment: button-counter;
  content: counter(button-counter);
  position: absolute;
  right: 0;
  bottom: 0;
  color: #d7e3e3;
  font-size: 12px;
  line-height: 1;
  padding: 5px;
}

.button-cover,
.knobs,
.layer {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
}

.button {
  position: relative;
  top: 50%;
  width: 74px;
  height: 36px;
  margin: -20px auto 0 auto;
  overflow: hidden;
}

.button.r,
.button.r .layer {
  border-radius: 100px;
}

.button.b2 {
  border-radius: 2px;
}

.checkbox {
  position: relative;
  width: 100%;
  height: 100%;
  padding: 0;
  margin: 0;
  opacity: 0;
  cursor: pointer;
  z-index: 3;
}

.knobs {
  z-index: 2;
}

.layer {
  width: 100%;
  background-color: #ebf7fc;
  transition: 0.3s ease all;
  z-index: 1;
}

/* Button 1 */
#button-1 .knobs:before {
  content: "YES";
  position: absolute;
  top: 4px;
  left: 4px;
  width: 20px;
  height: 10px;
  color: #fff;
  font-size: 10px;
  font-weight: bold;
  text-align: center;
  line-height: 1;
  padding: 9px 4px;
  background-color: #03a9f4;
  border-radius: 50%;
  transition: 0.3s cubic-bezier(0.18, 0.89, 0.35, 1.15) all;
}

#button-1 .checkbox:checked + .knobs:before {
  content: "NO";
  left: 42px;
  background-color: #f44336;
}

#button-1 .checkbox:checked ~ .layer {
  background-color: #fcebeb;
}

#button-1 .knobs,
#button-1 .knobs:before,
#button-1 .layer {
  transition: 0.3s ease all;
}

/* Button 2 */
#button-2 .knobs:before,
#button-2 .knobs:after {
  content: "YES";
  position: absolute;
  top: 4px;
  left: 4px;
  width: 20px;
  height: 10px;
  color: #fff;
  font-size: 10px;
  font-weight: bold;
  text-align: center;
  line-height: 1;
  padding: 9px 4px;
  background-color: #03a9f4;
  border-radius: 50%;
  transition: 0.3s ease all;
}

#button-2 .knobs:before {
  content: "YES";
}

#button-2 .knobs:after {
  content: "NO";
}

#button-2 .knobs:after {
  right: -28px;
  left: auto;
  background-color: #f44336;
}

#button-2 .checkbox:checked + .knobs:before {
  left: -28px;
}

#button-2 .checkbox:checked + .knobs:after {
  right: 4px;
}

#button-2 .checkbox:checked ~ .layer {
  background-color: #fcebeb;
}

/* Button 3 */
#button-3 .knobs:before {
  content: "YES";
  position: absolute;
  top: 4px;
  left: 4px;
  width: 20px;
  height: 10px;
  color: #fff;
  font-size: 10px;
  font-weight: bold;
  text-align: center;
  line-height: 1;
  padding: 9px 4px;
  background-color: #03a9f4;
  border-radius: 50%;
  transition: 0.3s ease all, left 0.3s cubic-bezier(0.18, 0.89, 0.35, 1.15);
}

#button-3 .checkbox:active + .knobs:before {
  width: 46px;
  border-radius: 100px;
}

#button-3 .checkbox:checked:active + .knobs:before {
  margin-left: -26px;
}

#button-3 .checkbox:checked + .knobs:before {
  content: "NO";
  left: 42px;
  background-color: #f44336;
}

#button-3 .checkbox:checked ~ .layer {
  background-color: #fcebeb;
}

/* Button 4 */
#button-4 .knobs:before,
#button-4 .knobs:after {
  position: absolute;
  top: 4px;
  left: 4px;
  width: 20px;
  height: 10px;
  color: #fff;
  font-size: 10px;
  font-weight: bold;
  text-align: center;
  line-height: 1;
  padding: 9px 4px;
  background-color: #03a9f4;
  border-radius: 50%;
  transition: 0.3s cubic-bezier(0.18, 0.89, 0.35, 1.15) all;
}

#button-4 .knobs:before {
  content: "YES";
}

#button-4 .knobs:after {
  content: "NO";
}

#button-4 .knobs:after {
  top: -28px;
  right: 4px;
  left: auto;
  background-color: #f44336;
}

#button-4 .checkbox:checked + .knobs:before {
  top: -28px;
}

#button-4 .checkbox:checked + .knobs:after {
  top: 4px;
}

#button-4 .checkbox:checked ~ .layer {
  background-color: #fcebeb;
}

/* Button 5 */
#button-5 {
  perspective: 60px;
  overflow: visible;
}

#button-5 .knobs:before,
#button-5 .knobs span {
  content: "";
  position: absolute;
  top: 4px;
  left: 4px;
  width: 20px;
  height: 10px;
  color: #fff;
  font-size: 10px;
  font-weight: bold;
  text-align: center;
  line-height: 1;
  padding: 9px 4px;
  border-radius: 50%;
  transition: 0.3s cubic-bezier(0.18, 0.89, 0.35, 1.15) all;
}

#button-5 .knobs:before {
  background-color: #03a9f4;
}

#button-5 .knobs span:before {
  content: "YES";
}

#button-5 .knobs:before,
#button-5 .layer {
  transform: rotateY(0);
  transform-origin: center;
}

#button-5 .checkbox:checked + .knobs:before,
#button-5 .checkbox:checked + .knobs span {
  left: 42px;
}

#button-5 .checkbox:checked + .knobs:before {
  transform: rotateY(180deg);
  background-color: #f44336;
}

#button-5 .checkbox:checked + .knobs span:before {
  content: "NO";
  left: 42px;
}

#button-5 .checkbox:checked ~ .layer {
  background-color: #fcebeb;
  transform: rotateY(-180deg);
}

#button-5 .knobs,
#button-5 .knobs:before,
#button-5 .layer {
  transition: 0.3s ease all;
}

/* Button 6 */
#button-6 {
  overflow: visible;
}

#button-6 .knobs:before {
  content: "YES";
  position: absolute;
  top: 4px;
  left: 4px;
  width: 20px;
  height: 10px;
  color: #fff;
  font-size: 10px;
  font-weight: bold;
  text-align: center;
  line-height: 1;
  padding: 9px 4px;
  background-color: #03a9f4;
  border-radius: 50%;
}

#button-6 .layer,
#button-6 .knobs,
#button-6 .knobs:before {
  transform: rotateZ(0);
  transition: 0.4s cubic-bezier(0.18, 0.89, 0.35, 1.15) all;
}

#button-6 .checkbox:checked + .knobs {
  transform: rotateZ(-180deg);
}

#button-6 .checkbox:checked + .knobs:before {
  content: "NO";
  background-color: #f44336;
  transform: rotateZ(180deg);
}

#button-6 .checkbox:checked ~ .layer {
  background-color: #fcebeb;
  transform: rotateZ(180deg);
}

/* Button 7 */
#button-7 .knobs:before,
#button-7 .knobs:after,
#button-7 .knobs span {
  position: absolute;
  top: 4px;
  width: 20px;
  height: 10px;
  font-size: 10px;
  font-weight: bold;
  text-align: center;
  line-height: 1;
  padding: 9px 4px;
  border-radius: 50%;
}

#button-7 .knobs:before {
  content: "YES";
  left: 4px;
  color: #fff;
  opacity: 1;
}

#button-7 .knobs:after {
  content: "N";
  left: 42px;
  color: #fff;
  width: 14px;
  text-align: left;
  padding: 9px 7px;
  background-color: #f44336;
  opacity: 0;
}

#button-7 .knobs:before,
#button-7 .knobs:after {
  transition: 0.3s ease all;
  z-index: 2;
}

#button-7 .knobs span {
  left: 4px;
  background-color: #03a9f4;
  transition: 0.2s ease all;
  z-index: 1;
}

#button-7 .checkbox:checked + .knobs:before {
  opacity: 0;
}

#button-7 .checkbox:checked + .knobs:after {
  opacity: 1;
}

#button-7 .checkbox:checked + .knobs span {
  top: 14px;
  left: 56px;
  width: 2px;
  height: 2px;
  padding: 3px;
  background-color: #fff;
  z-index: 3;
}

#button-7 .checkbox:checked ~ .layer {
  background-color: #fcebeb;
}

/* Button 8 */
#button-8 .knobs:before,
#button-8 .knobs:after,
#button-8 .knobs span {
  position: absolute;
  top: 4px;
  width: 20px;
  height: 10px;
  font-size: 10px;
  font-weight: bold;
  text-align: center;
  line-height: 1;
  padding: 9px 4px;
  border-radius: 50%;
  transition: 0.3s ease all;
}

#button-8 .knobs:before {
  content: "YES";
  color: #fff;
  left: 4px;
}

#button-8 .knobs:after {
  content: "NO";
  left: 42px;
  color: #fff;
  background-color: #f44336;
  opacity: 0;
}

#button-8 .knobs:before,
#button-8 .knobs:after {
  z-index: 2;
}

#button-8 .knobs span {
  left: 4px;
  background-color: #03a9f4;
  z-index: 1;
}

#button-8 .checkbox:checked + .knobs:before {
  opacity: 0;
}

#button-8 .checkbox:checked + .knobs:after {
  opacity: 1;
}

#button-8 .checkbox:checked + .knobs span {
  background-color: #fcebeb;
  transform: scale(4);
}

/* Button 9 */
#button-9 .knobs:before,
#button-9 .knobs:after,
#button-9 .knobs span {
  position: absolute;
  top: 4px;
  width: 20px;
  height: 10px;
  font-size: 10px;
  font-weight: bold;
  text-align: center;
  line-height: 1;
  padding: 9px 4px;
  border-radius: 50%;
  transition: 0.4s cubic-bezier(0.18, 0.89, 0.35, 1.15) all;
}

#button-9 .knobs:before {
  content: "YES";
  left: 4px;
}

#button-9 .knobs:after {
  content: "NO";
  right: -24px;
}

#button-9 .knobs:before,
#button-9 .knobs:after {
  color: #fff;
  z-index: 2;
}

#button-9 .knobs span {
  left: 4px;
  background-color: #03a9f4;
  z-index: 1;
}

#button-9 .checkbox:checked + .knobs:before {
  left: -24px;
}

#button-9 .checkbox:checked + .knobs:after {
  right: 4px;
}

#button-9 .checkbox:checked + .knobs span {
  left: 42px;
  background-color: #f44336;
}

#button-9 .checkbox:checked ~ .layer {
  background-color: #fcebeb;
}

/* Button 10 */
#button-10 .knobs:before,
#button-10 .knobs:after,
#button-10 .knobs span {
  position: absolute;
  top: 4px;
  width: 20px;
  height: 10px;
  font-size: 10px;
  font-weight: bold;
  text-align: center;
  line-height: 1;
  padding: 9px 4px;
  border-radius: 2px;
  transition: 0.3s ease all;
}

#button-10 .knobs:before {
  content: "";
  left: 4px;
  background-color: #03a9f4;
}

#button-10 .knobs:after {
  content: "NO";
  right: 4px;
  color: #4e4e4e;
}

#button-10 .knobs span {
  display: inline-block;
  left: 4px;
  color: #fff;
  z-index: 1;
}

#button-10 .checkbox:checked + .knobs span {
  color: #4e4e4e;
}

#button-10 .checkbox:checked + .knobs:before {
  left: 42px;
  background-color: #f44336;
}

#button-10 .checkbox:checked + .knobs:after {
  color: #fff;
}

#button-10 .checkbox:checked ~ .layer {
  background-color: #fcebeb;
}

/* Button 11 */
#button-11 {
  overflow: visible;
}

#button-11 .knobs {
  perspective: 70px;
}

#button-11 .knobs:before,
#button-11 .knobs:after,
#button-11 .knobs span {
  position: absolute;
  top: 4px;
  border-radius: 2px;
}

#button-11 .knobs:before,
#button-11 .knobs:after {
  width: 20px;
  height: 10px;
  color: #4e4e4e;
  font-size: 10px;
  font-weight: bold;
  text-align: center;
  line-height: 1;
  padding: 9px 4px;
}

#button-11 .knobs:before {
  content: "YES";
  left: 4px;
}

#button-11 .knobs:after {
  content: "NO";
  right: 4px;
}

#button-11 .knobs span {
  right: 4px;
  width: 33px;
  height: 28px;
  background-color: #03a9f4;
  transform: rotateY(0);
  transform-origin: 0% 50%;
  transition: 0.6s ease all;
  z-index: 1;
}

#button-11 .checkbox:checked + .knobs span {
  transform: rotateY(-180deg);
  background-color: #f44336;
}

#button-11 .checkbox:checked ~ .layer {
  background-color: #fcebeb;
}

/* Button 12 */
#button-12 .knobs:before,
#button-12 .knobs:after,
#button-12 .knobs span,
#button-12 .knobs span:before,
#button-12 .knobs span:after {
  position: absolute;
  top: 4px;
  font-size: 10px;
  font-weight: bold;
  text-align: center;
  line-height: 1;
  border-radius: 2px;
  transition: 0.3s ease all;
}

#button-12 .knobs:before {
  content: "YES";
  left: 4px;
}

#button-12 .knobs:after {
  content: "NO";
  right: 4px;
}

#button-12 .knobs:before,
#button-12 .knobs:after {
  width: 27px;
  height: 10px;
  color: #4e4e4e;
  padding: 9px 3px;
  z-index: 1;
}

#button-12 .knobs span {
  display: inline-block;
  z-index: 2;
}

#button-12 .knobs span,
#button-12 .knobs span:before,
#button-12 .knobs span:after {
  width: 20px;
  height: 10px;
  padding: 9px 4px;
}

#button-12 .knobs span:before,
#button-12 .knobs span:after {
  content: "";
  top: 0;
}

#button-12 .knobs span:before {
  left: -28px;
  background-color: #f44336;
}

#button-12 .knobs span:after {
  right: -42px;
  background-color: #03a9f4;
}

#button-12 .checkbox:checked + .knobs span:before {
  left: 4px;
}

#button-12 .checkbox:checked + .knobs span:after {
  right: -74px;
}

#button-12 .checkbox:checked ~ .layer {
  background-color: #fcebeb;
}

/* Button 13 */
#button-13 .knobs:before,
#button-13 .knobs:after,
#button-13 .knobs span {
  position: absolute;
  top: 4px;
  width: 20px;
  height: 10px;
  font-size: 10px;
  font-weight: bold;
  text-align: center;
  line-height: 1;
  padding: 9px 4px;
  border-radius: 2px;
  transition: 0.3s ease all;
}

#button-13 .knobs:before,
#button-13 .knobs:after {
  color: #4e4e4e;
  z-index: 1;
}

#button-13 .knobs:before {
  content: "YES";
  left: 4px;
}

#button-13 .knobs:after {
  content: "NO";
  right: 4px;
}

#button-13 .knobs span {
  width: 25px;
  left: 37px;
  background-color: #03a9f4;
  z-index: 2;
}

#button-13 .checkbox:checked + .knobs span {
  left: 4px;
  background-color: #f44336;
}

#button-13 .checkbox:checked ~ .layer {
  background-color: #fcebeb;
}

/* Button 14 */
#button-14 .knobs:before,
#button-14 .knobs:after,
#button-14 .knobs span:before,
#button-14 .knobs span:after {
  position: absolute;
  top: 4px;
  width: 20px;
  height: 10px;
  font-size: 10px;
  font-weight: bold;
  text-align: center;
  line-height: 1;
  padding: 9px 4px;
  border-radius: 2px;
  transition: 0.3s ease all;
}

#button-14 .knobs:before,
#button-14 .knobs:after {
  color: #4e4e4e;
  z-index: 1;
}

#button-14 .knobs:before {
  content: "YES";
  left: 4px;
}

#button-14 .knobs:after {
  content: "NO";
  right: 4px;
}

#button-14 .knobs span {
  top: 0;
  left: 0;
  display: block;
  width: 100%;
  height: 100%;
}

#button-14 .knobs span:before {
  left: 4px;
  top: -28px;
  background-color: #f44336;
}

#button-14 .knobs span:after {
  top: 4px;
  left: 39px;
  background-color: #03a9f4;
}

#button-14 .knobs span:before,
#button-14 .knobs span:after {
  content: "";
  width: 23px;
  z-index: 2;
}

#button-14 .checkbox:checked + .knobs span:before {
  top: 4px;
}

#button-14 .checkbox:checked + .knobs span:after {
  top: -28px;
}

#button-14 .checkbox:checked ~ .layer {
  background-color: #fcebeb;
}

/* Button 15 */
#button-15 .knobs:before,
#button-15 .knobs:after {
  position: absolute;
  top: 4px;
  width: 20px;
  height: 10px;
  color: #fff;
  font-size: 10px;
  font-weight: bold;
  text-align: center;
  line-height: 1;
  padding: 9px 4px;
  opacity: 1;
  border-radius: 2px;
  transform: scale(1);
  transition: 0.3s cubic-bezier(0.18, 0.89, 0.35, 1.15) all;
}

#button-15 .knobs:before {
  content: "YES";
  left: 4px;
  background-color: #03a9f4;
}

#button-15 .knobs:after {
  content: "NO";
  right: 4px;
  opacity: 0;
  transform: scale(4);
  background-color: #f44336;
}

#button-15 .checkbox:checked + .knobs:before {
  opacity: 0;
  transform: scale(4);
}

#button-15 .checkbox:checked + .knobs:after {
  opacity: 1;
  transform: scale(1);
}

#button-15 .checkbox:checked ~ .layer {
  background-color: #fcebeb;
}

/* Button 16 */
#button-16 .knobs:before {
  content: "YES";
  position: absolute;
  top: 4px;
  left: 4px;
  width: 20px;
  height: 10px;
  color: #fff;
  font-size: 10px;
  font-weight: bold;
  text-align: center;
  line-height: 1;
  padding: 9px 4px;
  background-color: #03a9f4;
  border-radius: 2px;
  transition: 0.3s ease all, left 0.3s cubic-bezier(0.18, 0.89, 0.35, 1.15);
}

#button-16 .checkbox:active + .knobs:before {
  width: 46px;
}

#button-16 .checkbox:checked:active + .knobs:before {
  margin-left: -26px;
}

#button-16 .checkbox:checked + .knobs:before {
  content: "NO";
  left: 42px;
  background-color: #f44336;
}

#button-16 .checkbox:checked ~ .layer {
  background-color: #fcebeb;
}

/* Button 17 */
#button-17 .knobs:before,
#button-17 .knobs span {
  content: "YES";
  position: absolute;
  top: 4px;
  left: 4px;
  width: 20px;
  height: 10px;
  color: #fff;
  font-size: 10px;
  font-weight: bold;
  text-align: center;
  line-height: 1;
  padding: 9px 4px;
}

#button-17 .knobs:before {
  transition: 0.3s ease all, left 0.5s cubic-bezier(0.18, 0.89, 0.35, 1.15);
  z-index: 2;
}

#button-17 .knobs span {
  background-color: #03a9f4;
  border-radius: 2px;
  transition: 0.3s ease all, left 0.3s cubic-bezier(0.18, 0.89, 0.35, 1.15);
  z-index: 1;
}

#button-17 .checkbox:checked + .knobs:before {
  content: "NO";
  left: 42px;
}

#button-17 .checkbox:checked + .knobs span {
  left: 42px;
  background-color: #f44336;
}

#button-17 .checkbox:checked ~ .layer {
  background-color: #fcebeb;
}

/* Button 18 */
#button-18 .knobs:before,
#button-18 .knobs span {
  content: "YES";
  position: absolute;
  top: 4px;
  left: 4px;
  color: #fff;
  font-size: 10px;
  font-weight: bold;
  text-align: center;
  line-height: 1;
  background-color: #03a9f4;
  border-radius: 2px;
}

#button-18 .knobs:before {
  top: 50%;
  left: 8px;
  width: 20px;
  height: 10px;
  margin-top: -5px;
  background-color: transparent;
  z-index: 2;
}

#button-18 .knobs span {
  width: 20px;
  height: 10px;
  padding: 9px 4px;
  transition: 0.3s ease all, left 0.3s cubic-bezier(0.18, 0.89, 0.35, 1.15);
  z-index: 1;
}

#button-18 .checkbox:active + .knobs:before {
  left: 10px;
  width: 46px;
  height: 4px;
  color: transparent;
  margin-top: -2px;
  background-color: #0095d8;
  transition: 0.3s ease all;
  overflow: hidden;
}

#button-18 .checkbox:active + .knobs span {
  width: 58px;
}

#button-18 .checkbox:checked:active + .knobs:before {
  left: auto;
  right: 10px;
  background-color: #d80000;
}

#button-18 .checkbox:checked:active + .knobs span {
  margin-left: -38px;
}

#button-18 .checkbox:checked + .knobs:before {
  content: "NO";
  left: 47px;
}

#button-18 .checkbox:checked + .knobs span {
  left: 42px;
  background-color: #f44336;
}

#button-18 .checkbox:checked ~ .layer {
  background-color: #fcebeb;
}



Resources
