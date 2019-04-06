# README

Course website for CS 498 Virtual Reality at the University of Illinois.

## Getting Started

* [Install Jekyll](https://jekyllrb.com/docs/installation/)
* `cd` to the location of the cloned repo
* Run `bundle install` for dependencies
* Run `bundle exec jekyll serve` to start the website, then visit [`http://localhost:4000`](http://localhost:4000).

## Random Documentation

Stuff that doesn't really fit elsewhere.

### Managing the class schedule

In `_data/schedule.yml` there is a list of objects, each representing one class. Each one must contain the following fields:

- `date`: string containing the date of the lecture (formatted like so: `"27 Aug 2018"`)
- `materials`: string, will be markdownified. Should contain relevant textbook chapters to that lecture and optionally any 
extra materials.
- `title`: string, will be markdownified. Should link to the slides.

### Using Collapsible Sections

The scripts are provided in `/assets/collapse-sections.js`. Include it near the bottom of your layout, and then call it with `sections(container)` where `container` is the `querySelector` for the scope of your content (for example, if all the content is in a div with a class name of `wrapper`, you would pass in `.wrapper`). For an example, see `/_layouts/assignment.html`.

You will also need to import the styles. These are defined in `_sass/sections.scss`. To use them, simply `@import` them into the appropriate scope of your scss file. For an example, see `/_scss/assignment.scss`. 