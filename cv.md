## Personal information and contacs
* Name Igor Minaev
* Email igormin81@mail.ru
* Phone number: +7-917-114-5515
* Discord: grigoran#7524
## About
At this moment, code is my hobby. I don't have any commercial experience with coding, but i enjoy it and want to make it my profession.
I always educate myself and try to improve my skills in programming field. I can easily find information, required to solve any tasks.
In this way, i want to work in this industry.
## Skills
* js/HTML/css
    * BEM
* c++
    * sfml
    * makefile
* Visual Studio
* Visual Studio Code
* QtCreator
* linux terminal

## Code examples
```c++
//code fragment from https://github.com/grigoran/Dots.git
bool Dot::findPath(Node *node, Node *start, int num) {
  sf::Vector2i index = node->getIndex();
  Node *getedNode;
  node->mark();
  for (int i = 0; i < 8; i++) {
    getedNode = nodes.get(index, i);
    if (getedNode == start && num > 2) {
      node->conect(node, getedNode);
      node->unmark();
      return true;
    }
    if (getedNode->Team() == start->Team() && !getedNode->isConected() &&
        !getedNode->isMarked()) {
      if (findPath(getedNode, start, num + 1)) {
        node->conect(node, getedNode);
        node->unmark();
        return true;
      }
    }
  }
  node->unmark();
  return false;
}
```
```js
//code fragment from https://github.com/grigoran/portfolioSite.git
let slider__circles = document.querySelectorAll(".slider__circle");
slider__circles[0].style["r"] = 5;

let slider__images = document.querySelector(".slider__images");
let slider__image = document.querySelectorAll(".slider__image");
let imageCount = slider__image.length;
let slider__arrow = document.querySelectorAll(".slider__arrow");
let nowImage = 0;
let offset = 0;



slider__images.style.width = imageCount * 300 + "px";

document.addEventListener("DOMContentLoaded", () => {
    setTimeout(() => {
        slider__arrow.item(0).style.opacity = "0%";
        slider__arrow.item(1).style.opacity = "0%";
    }, 350)
})
function getIndex(index) {
    return ((index + imageCount) % imageCount);
}

slider__arrow.item(0).addEventListener("click", () => {
    slider__circles[nowImage].style["r"] = 3;
    nowImage = getIndex(nowImage - 1);
    slider__circles[nowImage].style["r"] = 5;
    offset = -nowImage * 300;
    slider__images.style["margin-left"] = offset + "px";
});
slider__arrow.item(1).addEventListener("click", () => {
    slider__circles[nowImage].style["r"] = 3;
    nowImage = getIndex(nowImage + 1);
    slider__circles[nowImage].style["r"] = 5;
    offset = -nowImage * 300;
    slider__images.style["margin-left"] = offset + "px";
});
```

## Projects
* [Own website](https://github.com/grigoran/portfolioSite.git)
* [Dots game writen on c++/sfml](https://github.com/grigoran/Dots.git)

## Languages
* Russian: native
* English: B2
