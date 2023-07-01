- [inset](#inset)
- [clamp-function](#clamp-function)
- [scroll-snap-type-and-scroll-snap-align](#scroll-snap-type-and-scroll-snap-align)
- [display-block--inline--inline-block--flex--inline-flex](#display-block--inline--inline-block--flex--inline-flex)
- [css-logical-properties](#css-logical-properties)
- [css-advance-selectors--pseudo-classes](#css-advance-selectors--pseudo-classes)
- [line-clamp-and-text-overflow-ellipsis](#line-clamp-and-text-overflow-ellipsis)
- [min--max](#min--max)
- [writing-mode-text-orientation-and-direction](#writing-mode-text-orientation-and-direction)
- [typography](#Typography)
- [color-mix-function-and-nested-css](#color-mix-function-and-nested-css)
- [first-letter-pesudo-element](#first-letter-pesudo-element)
- [-webkit-background-clip-text](#-webkit-background-clip-text)

<hr />

### `inset`
 - Without explicitly providing height and width to .child - achieved same work using `inset` -  shorthand of [top, right, bottom, left]

![Screenshot 2023-06-28 at 3 18 02 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/9de5fb62-06bb-4766-8d03-af45c249ed4a)
![Screenshot 2023-06-28 at 2 56 28 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/b130272f-efe9-4cba-9748-5a5163daf138)

<hr />

## `clamp` function
 - shorthand of [min-width, width, max-width]

![Screenshot 2023-06-28 at 3 27 31 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/3a3f0c85-e235-4bbf-b2bd-855e4b8c4ba6)
![Screenshot 2023-06-28 at 3 28 25 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/d5cac9e4-1e7e-41d4-be47-672c36b8a3fd)
![Screenshot 2023-06-28 at 3 27 44 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/8bd506b5-0173-4166-8ce2-6e57ad55f591)
![Screenshot 2023-06-28 at 3 28 45 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/1157a402-8375-492e-9371-b98e53128b14)

<hr />

### `scroll-snap-type` and `scroll-snap-align`
 - Based on scroll element scrolled-percentage, auto Snap to the Center, just like any other reels app

![Screenshot 2023-06-28 at 11 33 12 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/286a5bf5-790c-4c5a-811b-bb44e848fbf2)

![Screenshot 2023-06-28 at 11 34 06 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/416a855d-febb-4ea5-8422-126701d439f7)

![Screenshot 2023-06-28 at 11 40 10 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/e98d93c1-4b87-4bb7-8b42-846f92c732ad)

<hr />

## `display: block | inline | inline-block | flex | inline-flex`

 - `display: block;` takes complete (block), full width, even you explicitly provide width to it

    - ![Screenshot 2023-06-29 at 11 25 54 AM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/2eac26fa-0f79-41a0-a7c1-5279e8d948f7)

    - ![Screenshot 2023-06-29 at 11 25 44 AM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/cc7009c7-2f34-46d5-a4c7-6994b701372b)

- `display: inline;` takes width as per content height-width init, and other rest elements placed side by side, but we can’t provide height-width explicitly to them

    - ![Screenshot 2023-06-29 at 11 31 25 AM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/1a4dfbba-1d9b-4fbb-bdca-49c563077ca1)

    - ![Screenshot 2023-06-29 at 11 31 44 AM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/6c0d3b58-ff65-4e4b-8c7b-882f52c4d91b)

 - `display: inline-block;` act as inline (elements side by side) but also takes height-width explicitly

    - ![Screenshot 2023-06-29 at 11 36 14 AM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/45813bb0-a2f0-4444-ae26-3aff37e909b2)

    - ![Screenshot 2023-06-29 at 11 36 36 AM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/550e6665-6748-4450-89f8-5b8236f24e33)

 - `display: flex;` makes container/parent flexBox and all Childs flex-items, side by side elements, items act as inline-block, and container takes full width, container width (taking full width/block concept) act same as display: block

     - ![Screenshot 2023-06-29 at 11 42 55 AM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/cf4bf884-ccf7-40bc-ba01-50ecbafacf21)
  
     - ![Screenshot 2023-06-29 at 11 43 22 AM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/10483b60-3c50-4467-bf3d-9b6deb8e6d8a)

 - `display: inline-flex;` complete act as flexBox container but only difference is, the container act as inline-block, not takes will block width, only takes as per content init

     - ![Screenshot 2023-06-29 at 11 47 54 AM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/355951f0-159c-494a-836c-09c4385c7ab4)
  
     - ![Screenshot 2023-06-29 at 11 47 34 AM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/f23b89d8-ce90-4d50-be8a-7577f640b850)

     - ![Screenshot 2023-06-29 at 11 48 56 AM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/ce2a5369-3606-4bfb-9d75-fae4275245ab)

     -  ![Screenshot 2023-06-29 at 11 49 09 AM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/4889729e-699d-4913-a96f-24130089f384)

<hr />

## CSS logical properties

- `margin-inline, margin-block, padding-inline, padding-block, border-block, border-inline`

### Very helpfull when working with directions, instead of providing padding-left use padding-inline-start, this will auto apply padding-left no metter what text directions we're using (still work, no metter, we chaned the direction), hard to achieve this with using padding-left direct.

 - ![Screenshot 2023-06-29 at 12 15 37 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/97210dc4-699a-4be1-b79d-c3246654cdb3)

 - ![Screenshot 2023-06-29 at 12 16 24 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/478d851f-7b88-4247-9283-ae497b954423)

<hr />

## CSS advance selectors + PSEUDO-classes

- `>` use to select all direct child elements
 
- `+` use to select immediate sibling element
 
- PSEUDO-classes
    - `:has` use to conditionally select element which has some (conditional-child-element), use to apply css on that parent
    - and `:is` use to select multiple elements, (many childs), shorthand (as shown bellow)

    - ![Screenshot 2023-06-29 at 1 21 27 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/b154f9e8-46a9-4e94-9377-5ab12138bb92)

    - ![Screenshot 2023-06-29 at 1 22 16 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/9d64debb-ed0b-4bdc-985b-32ac4cf058bc)

<hr />

##  `line-clamp` and `text-overflow: ellipsis;`

 - ![Screenshot 2023-06-29 at 1 28 38 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/fa2397a1-465b-4907-ba6a-325d6ce471b2)
 
 - ![Screenshot 2023-06-29 at 1 29 09 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/6659fc22-8f68-4a58-86af-04e7e7287482)

 - ![Screenshot 2023-06-29 at 1 30 01 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/16b93615-3a98-45cd-95a1-5aa1f9f51243)

-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-

 - ![Screenshot 2023-07-01 at 4 06 53 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/a886e328-4c69-418e-bc9c-d8d8eece71f9)

 - ![Screenshot 2023-07-01 at 3 47 49 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/eadd6bfa-5109-4369-b3e8-a8936fe92a22)

<hr />

## `min & max`

- function, shorthand of `width + min-width` and `width + max-width`

- ![Screenshot 2023-06-29 at 2 35 51 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/476e09a1-67b7-44e2-8fc3-399379af6805)

- this will choose min out of both based of screen-size (in realtime)
  ```
   /* width: 8%;
   min-width: 73px; */
   width: min(8%, 73px);
  ```

<hr />

## `writing-mode`, `text-orientation` and `direction`

 - ![Screenshot 2023-06-29 at 7 51 25 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/5d4f1b9f-3e79-47db-99d1-fd31a90981b0)

 - ![Screenshot 2023-06-29 at 7 51 35 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/93609778-0fc8-4aed-a5ab-13b4a59a27b1)

 - ![Screenshot 2023-06-29 at 8 36 56 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/7dfab254-53c2-4e04-a949-9b0caeb3c3ad)

 - ![Screenshot 2023-06-29 at 8 37 19 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/5a506ff9-c552-4642-9606-d7212de1c5c6)

<hr />

## Typography

 - heading
   - letter-spacing: 0.4rem | -0.4rem; based on heading complete uppercase (0.4rem) or lowercase(-0.4rem)
   - font-size: clamp(2rem, 8vw, 6rem);
   - line-height: 1.1; when working with H1 - H6 headings | gap vertically between lines
   - ![Screenshot 2023-06-30 at 4 56 12 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/1057f860-fd76-4ca6-86f7-9563201647b2)

 - paragraph
   - max-width: 50ch; ch - characters | must be between 50 to 70 ch
   - text-wrap: balance;
    
 - anchor
   - text-decoration-color: if text color is dark then choose this as light a bit
   - text-decoration-thickness: 2px;
   - text-underline-offset: 4px;

 - [ ol / ul ] - li
   - ![Screenshot 2023-06-30 at 4 50 56 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/1451d242-4346-40a8-86df-1c5fbe9dc825)
   - aligh text to text | or :: marker to text | (object to object - rule of thumb)

<hr />

## `color-mix` function and nested css

  - ![Screenshot 2023-06-30 at 6 53 56 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/d1b1c647-fd8f-433e-af0f-3d70806b8efe)
  - ![Screenshot 2023-06-30 at 6 54 38 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/d5c0b268-b999-42cf-afba-6308ae4f3a09)

<hr />

## `::first-letter` pesudo element

 - ![Screenshot 2023-06-30 at 7 11 53 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/ae2fa379-f38b-4427-9fde-536c684c91cb)

 - ![Screenshot 2023-06-30 at 7 12 07 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/e27e8970-2a7d-427b-86a3-6702529c6050)

<hr />

## `-webkit-background-clip: text;`

 - ![Screenshot 2023-07-01 at 4 04 25 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/67864865-56ed-4453-8196-44966ea4b04e)

 - ![Screenshot 2023-07-01 at 4 04 35 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/7a1ef96c-e11e-4d60-b6f7-85c452979280)

-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-X-

 - ![Screenshot 2023-07-01 at 4 51 09 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/b5469c90-eab6-4e0a-8fff-b508fd3ce3d5)

 - ![Screenshot 2023-07-01 at 4 51 33 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/e7705a34-ced3-4cb8-9b21-6dc495ab22c3)

<hr />
