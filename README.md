# adapt-draganddrop

**Drag and Drop** is a *presentation component* Created by Dan storey.

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

**_attempts** (integer): This specifies the number of times a learner is allowed to submit an answer. The default is `1`.

**_shouldDisplayAttempts** (boolean): Determines whether or not the text set in **remainingAttemptText** and **remainingAttemptsText** will be displayed. These two attributes are part of the [core buttons](https://github.com/adaptlearning/adapt_framework/wiki/Core-Buttons) attribute group. The default is `false`.

**_canShowModelAnswer** (boolean): Setting this to `false` prevents the [**_showCorrectAnswer** button](https://github.com/adaptlearning/adapt_framework/wiki/Core-Buttons) from being displayed. The default is `true`.

**_recordInteraction** (boolean) Determines whether or not the learner's answer(s) will be recorded on the LMS via cmi.interactions. Default is `true`. For further information, see the entry for `_shouldRecordInteractions` in the README for [adapt-contrib-spoor](https://github.com/adaptlearning/adapt-contrib-spoor).

**_questionWeight** (number): A number which reflects the significance of the question in relation to the other questions in the course. This number is used in calculations of the final score reported to the LMS.

**_feedback** (object): If the [**Tutor** extension](https://github.com/adaptlearning/adapt-contrib-tutor) is enabled, these various texts will be displayed depending on the submitted answer. **_feedback**
contains values for three types of answers: **correct**, **_incorrect**, and **_partlyCorrect**. Some attributes are optional. If they are not supplied, the default that is noted below will be used.

>**correct** (string): Text that will be displayed when the submitted answer is correct.

>**_incorrect** (object): Texts that will be displayed when the submitted answer is incorrect. It contains values that are displayed under differing conditions: **final** and **notFinal**.

>>**final** (string): Text that will be displayed when the submitted answer is incorrect and no more attempts are permitted.

>>**notFinal** (string): Text that will be displayed when the submitted answer is incorrect while more attempts are permitted. This is optional&mdash;if you do not supply it, the **_incorrect.final** feedback will be shown instead.

>**_partlyCorrect** (object): Texts that will be displayed when the submitted answer is partially correct. It contains values that are displayed under differing conditions: **final** and **notFinal**.

>>**final** (string): Text that will be displayed when the submitted answer is partly correct and no more attempts are permitted. This is optional&mdash;if you do not supply it, the **_incorrect.final** feedback will be shown instead.

>>**notFinal** (string): Text that will be displayed when the submitted answer is partly correct while more attempts are permitted. This is optional&mdash;if you do not supply it, the **_incorrect.notFinal** feedback will be shown instead.

### Accessibility

## Limitations

Viewport sizing

----------------------------
**Version number:**  1.0
**Framework versions:**  2.0
**Author / maintainer:** Dan Storey
