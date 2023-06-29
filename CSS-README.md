### `inset`
 - Without explicitly providing height and width to .child - achieved same work using `inset` -  shorthand of [top, right, bottom, left]

![Screenshot 2023-06-28 at 3 18 02 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/9de5fb62-06bb-4766-8d03-af45c249ed4a)
![Screenshot 2023-06-28 at 2 56 28 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/b130272f-efe9-4cba-9748-5a5163daf138)

<hr />

## `clamp` function
 - shorthand of [min-width, width, max-width]

![Screenshot 2023-06-28 at 3 28 25 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/d5cac9e4-1e7e-41d4-be47-672c36b8a3fd)
![Screenshot 2023-06-28 at 3 27 44 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/8bd506b5-0173-4166-8ce2-6e57ad55f591)
![Screenshot 2023-06-28 at 3 28 45 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/1157a402-8375-492e-9371-b98e53128b14)
![Screenshot 2023-06-28 at 3 27 31 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/3a3f0c85-e235-4bbf-b2bd-855e4b8c4ba6)

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

## CSS logical properties, `margin-inline, margin-block, padding-inline, padding-block, border-block, border-inline`

 - ![Screenshot 2023-06-29 at 12 15 37 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/97210dc4-699a-4be1-b79d-c3246654cdb3)

 - ![Screenshot 2023-06-29 at 12 16 24 PM](https://github.com/workLokeshVishwakarma/learning-notes/assets/121422811/478d851f-7b88-4247-9283-ae497b954423)

<hr />
