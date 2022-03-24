# Front-end tech test

Please note, you do not have to complete all of the below. Please spend **no more than 2 hours** on this task. 

## Problem

You have a 5x5 grid that represents islands on a map. This grid can be randomly generated. An example:

```
0 1 1 1 1
0 0 1 0 1
0 0 0 0 0 
0 1 0 0 0
0 1 0 0 0
```

In this grid, `1` means land, and `0` means water.

From this grid, a number of complete islands can be calculated. An island is any area of land surrounded by water and is formed by connecting adjacent lands horizontally or vertically. You can assume that the map is surrounded by water.

For example, the number of islands in the above map is **2**.

## Task

Create an application that will:

### 1. Render HTML output for data with the following structure:

```ts
type IslandsOutput = {
    map: number[][],
    islands: number,
};
```

- `map` is a randomly generated 5x5 grid of 1s and 0s. 1s represent land and 0s represent water.
- `islands` is the number of islands in the map. An island is any area of land surrounded by water and is formed by connecting adjacent lands horizontally or vertically. You can assume that the map is surrounded by water.

**Examples:**

```json
{
    "map": [
        [0,1,1,1,1],
        [0,0,1,0,1],
        [0,0,0,0,0],
        [0,1,0,0,0],
        [0,1,0,0,0],
    ],
    "islands": 2
}
```
```json
{
    "map": [
        [1,0,1,1,0],
        [1,1,0,0,0],
        [1,1,0,1,0],
        [0,1,0,0,0],
        [1,1,0,0,0],
    ],
    "islands": 3
}
```

You may choose how to render this in HTML. We'd recommend making use of a front-end framework, for example, [React](https://reactjs.org/).

### 2. Generate a random map

Create a function to generate the random 5x5 grid.

### 3. Write the island counting algorithm

Write an algorithm that given the 5x5 grid will return the number of islands within it. e.g.

```ts
const grid = [
    [1,0,1,1,0],
    [1,1,0,0,0],
    [1,1,0,1,0],
    [0,1,0,0,0],
    [1,1,0,0,0],
];

const islands = countIslands(grid);
console.log(islands);
// 3
```

### General tips / requirements

* Although it may seem unnecessary for this project, you must use Typescript and can make use of any open source libraries which you think may help. You should comment your code with your thought process and reasoning.
* Tests are recommended.
* Ideally the application will be contained in a Docker container. Please provide any execution instructions.
* You may use 3rd party code, but please note where you've done this.
* **You do not have to complete the whole task** - you don't need to spend more than **two hours** on this as we don't want to use up too much of your time on a throw away application. If you do run out of time or can't spare that much time, instead note how long you spent, any sticking points and what you would have done given more time. Likewise, if you do spend more time than mentioned, then please mention how long and your reasons for continuing.

Once you're done, you can zip your source files and email it and a summary of your experience to us via your recruiter.
