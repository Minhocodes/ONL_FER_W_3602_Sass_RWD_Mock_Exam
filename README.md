![Coders-Lab-1920px-no-background](https://user-images.githubusercontent.com/30623667/104709394-2cabee80-571f-11eb-9518-ea6a794e558e.png)

# Important information

Read the following guidelines before doing the exercises.

## How do you begin?

1. [*Fork*](https://guides.github.com/activities/forking/) the repository containing exercises.
2. Clone the repository onto your computer using the command: `git clone repository_address`.
   You will find the address of the repository by pressing "Clone or download" button on its webpage.
3. Complete the exercises and commit changes to your repository using the commands below.
   `git add filename` will add a single file which you have changed.
   If you want to add all the changed files at once, use `git add .`.
   Remember that the fullstop (dot) at the end of this command is important!
   Next, commit changes using `git commit -m "description_of_changes"`.
4. Push changes to your repository on GitHub by typing: `git push origin main`.
5. Create a [*pull request*](https://help.github.com/articles/creating-a-pull-request) to the original repository when you have finished all the exercises.

### Do the exercises in appropriate files.

**The repository with the exercises will be removed 2 weeks after the end of the course. This will result in the removal of all forks made from this repository.**


> ### Notes to the exam
> 1. Complete tasks in appropriate files in the `scss/partials` catalog (e.g.: `scss/partials/_task01.scss`).
> 1. There is a ```main.scss``` file that imports all tasks prepared for you.
> 1. Save the result of `scss/main.scss` compilation in the `scss/main.scss` file - do not change the file and directory structure!


## Task 1

Create a simple CSS reset in the `scss/partials/_task01.scss` file.


## Task 2

In the `scss/partials/_task02.scss` file, create a **map** of 5 colors:

* gold - `#f9c00c`
* blue - `#00b9f1`
* purple - `#7200da`
* red - `#f9320c`
* green - `#75D701`

Using interpolation and loop, assign the above colors as backgrounds of elements with classes `el-1`, `el-2`, etc. that are placed in the section with `task-02` class.

Using flex, align those elements next to one another. Each element should be `200px` wide.

Remember to use appropriate Sass modules (`@use`)!


## Task 3

Create a mixin named ```arrow```. It should take __3__ parameters ```$color```, ```$direction```, ```$size```.
The aim of the mixin is to create an arrow of a given color, direction and size.


Call the prepared mixin for **4 prepared elements** in the section with `task-03` class according to their class names, e.g. `arrow-test-blue-top-20px`: is a blue arrow facing upwards with dimensions: `20px` x `20px`:

```scss
.arrow-test {
  &-blue-top-20px {
    @include arrow(blue, top, 20px);
  }
}
```


__Hints:__
* do not use pseudo-elements
* mixin name is ```arrow```, do not change it!
* the order of the parameters should be exactly as in the example of the call ($color, $direction, $size)


## Task 4

Using variables and loop, create all classes necessary for making your own grid.

We assume that grid will have 10-column layout, and the main container will have the width of `1200px`.

Name the classes connected with element width `.col-X` - for example `.col-1`, `.col-2` ... `.col-10`. Don't forget about `container` and `row` classes.

Based on the created grid, recreate the following layout in the section with the `task-04` class:

![](images/layout.png)

You should use **colors from the map** created in the second task!

- Logo: color under the `red` key
- Navigation: color under the `red` key brightened by `30%` (use appropriate function)
- Slider: color under the `blue` key
- Box: color under the `gold` key
- Copyright: color under the `green` key darkened by `30%` (use appropriate function)
- Menu: color under the `green` key


## Task 5

The section with `task-05` class contains an image. Set `100vh` height for this section.

Next, describe appropriate conditions so that:
* When the screen is `1025px` or wider, the image has the width of `600px` and is **centered in the section** (both vertically and horizontally),
* When the screen width is between `768px` and `1024px` (including those values), the image has the width of `200px` and is placed in the **top right corner of the section**,
* When the screen is `767px`or narrower, the image has **all available width** of the section.

**Stick to the Mobile First convention**!

Remember that the image should always have **the same proportions** (it cannot be stretched vertically or horizontally)!

Use **flexbox** only.
