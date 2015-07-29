---
title: Haushalt Design
layout: post
author: judith
abstract: Design decisions for Haushalt
---

# Data Model
![Haushalt data model](https://raw.github.com/lambda-kollektiv/haushalt/master/design/haushalt-datamodel.pdf)


# User Interface

The user interface will be modular consisting of a pin board where a user can place an arbitrary number of widgets. Widgets will show input forms, tables, statistics or whatever the user wants to have quick access to. The different widget types will have different variations, so sometimes it will make sense to have multiple widgets of the same type on one board.

A widget takes two arguments: the global state and its configuration, both being hash-maps that need to define certain keys depending on the widget type.


```
(generic-widget global-state configuration)
```

## Input Widget
Widget for adding data like new expenses or revenues.

Necessary keys for input maps:

- **Global state:** _none_
  Further possibly useful entries:
  - companies, expenses, revenues if auto-completion or suggestions are implemented

- **Configuration:** _type, detailed_
  - **type:** "expense" | "revenue", default: "expense"
  - **detailed:** false | true, default: false
  Further possible configurations:
  - design specifics

**Effect:** global state changes

## Table Widget
Shows expenses and revenues ordered by configurable criteria.

Necessary keys for input maps:

- **Global state:** _expenses, revenues_

- **Configuration:** _expenses, revenues, detailed, sort-key, ascending_
  - **expenses:** true | false, default: true
  - **revenues:** true | false, default: true
  - **detailed:** false | true, default: false
  - **sort-key:** date | category | ..., default: date
  - **ascending:** false | true, default: false

**Effect:** none
- if editing is permitted: global state changes

## Summary Widget
Shows bar diagram of expenses and revenues of one or multiple time periods.

Necessary keys for input maps:

- **Global state:** _expenses, revenues_

- **Configuration:** _type, categories, period, compare_
  - **type:** "all" \| "expenses" | "revenues" , default: "all"
  - **categories:** true | false, default: true
    - bar diagram becomes
  - **period:** [0-8]+, default: 30 (in days)
  - **compare:** true | false, default: true
    - compare to previous time period
  Further possible configurations:
  - design specifics

**Effect:** none

## Timeline Widget
Shows cash flow over time.

Details:
Shows expense/revenue on hovering over line, maybe exact date/time when hovering over point

Necessary keys for input maps:

- **Global state:** _none_

- **Configuration:** _zero_
  - **zero:** [0-9]+, default: 0
    - chosen line where budget is zero, assumption for deault: user starts with no budget
  Further possible configurations:
  - design specifics

**Effect:** none
