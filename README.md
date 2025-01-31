# framer-motion-carousel

A simple `framer-motion-carousel`, used for `framer-motion`, `chakra-ui`
support `click` and `swipe`, support custom `arrows`, `dots`, easy to use.
## Basic Usage

```jsx
import * as React from "react";
import Carousel from "framer-motion-carousel";

const colors = ["#f90", "#ef0", "#e0f"];

const App = () => (
  <div style={{ width: 600, height: 400 }}>
    <Carousel>
      {colors.map((item, i) => (
        <div
          key={i}
          style={{
            width: "100%",
            height: "100%",
            backgroundColor: colors[i],
          }}
        ></div>
      ))}
    </Carousel>
  </div>
);
export default App;
```

## images carousel

`img` element should add `draggable=false`

```jsx
<div style={{ width: 600, height: 400, margin: "0 auto" }}>
  <Carousel>
    {[1, 2, 3, 4].map((item, i) => (
      <img
        draggable="false"
        src={`./${item}.jpg`}
        key={i}
        width="100%"
        alt=""
      />
    ))}
  </Carousel>
</div>
```

## Example

[Live Demo](https://carousel-app-772051431.vercel.app)

![example](https://raw.githubusercontent.com/jiangbo2015/framer-motion-carousel/main/img.jpg)


## props

| props            | type                                                                                 | default | description        |
|------------------|--------------------------------------------------------------------------------------|---------|--------------------|
| loop             | boolean                                                                              | true    | loop play          |
| autoPlay         | boolean                                                                              | true    | auto play          |
| interval         | number                                                                               | 2000    | auto play interval |
| renderArrowLeft  | ({handlePrev: () => void, activeIndex: number}) => React.ReactNode                   | null    | custom your arrows |
| renderArrowRight | ({handleNext: () => void, activeIndex: number}) => React.ReactNode                   | null    | custom your arrows |
| renderDots       | ({activeIndex: number, setActiveIndex: (index: number) => void;}) => React.ReactNode | null    | custom your dots   |



## Development

```
yarn install

yarn build
```