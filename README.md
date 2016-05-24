# adapt-draganddrop

**Drag and Drop** is a *presentation component* Created by Dan storey.
<img align="right" src="https://raw.githubusercontent.com/danielstorey/adapt-resources/master/draganddrop-demo.jpg" alt="Drag and Drop Question Component">

A learner must drag the correct answers to the relevant questions. This plug in supports dummy answers and multiple correct answers for each question. the order the answers appear in is random each time the user loads the page so there is no way of telling the dummy answers appart from the correct ones. Configuration is incredibly simple as you will see from the [*example*](https://github.com/danielstorey/adapt-draganddrop/example.json).

##Installation

## Settings Overview

The attributes listed below are used in *components.json* to configure **Drag and Drop**, and are properly formatted as JSON in [*example.json*](https://github.com/danielstorey/adapt-draganddrop/example.json).

### Attributes

[**core model attributes**](https://github.com/adaptlearning/adapt_framework/wiki/Core-model-attributes): These are inherited by every Adapt component. [Read more](https://github.com/adaptlearning/adapt_framework/wiki/Core-model-attributes).

**_component** (string): This value must be: `draganddrop`. (One word.)

**_classes** (string): CSS class name to be applied to **Drag and Drop** containing `div`. The class must be predefined in one of the Less files. Separate multiple classes with a space.

**_layout** (string): This defines the horizontal position of the component in the block. Acceptable values are `full`, `left` or `right`.

**instruction** (string): This optional text appears above the component. It is frequently used to
guide the learner’s interaction with the component.

**title** (string): This is the title text for the **Drag and Drop** component.

**body** (string): This is the main text for the **Drag and Drop** component.

**_items** (string): Each item represents a question for this component and contains values for **_text** and **_accepted**.

>**_text** (string): The text to be displayed for the question.

>**_accepted** (mixed): Accepted answers can either be a string for a single answer or an array for multiple answers.

**dummyAnswers** (array): Optional dummy answers to add to the mix.

**animationTime** (number): The time in ms for the animations to take place. Default is 200.

**animationDelay** (number): The delay in between answers being animated when switching between the learner's answer and the correct answer. Default is 0 - all answers move at the same time.

### Accessibility

### Limitations

Not currently responsive

Viewport sizing

----------------------------
**Version number:**  1.0
**Framework versions:**  2.0
**Author / maintainer:** Dan Storey
