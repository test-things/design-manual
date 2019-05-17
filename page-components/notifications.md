---
title: Notifications
date: 2019-05-17T20:48:07.960Z
implementation-status: released
description: >-
  # Notifications


  Where possible, display formatting errors immediately using client-side
  validation so the user doesn’t have to wait until submitting to see what went
  wrong (this is especially frustrating if the information the user enters the
  first time around is not cached on submit and they have to fill out all the
  fields again from scratch). If letters are entered in a date field, if an
  email address is missing the “@” sign, let the user know right away by showing
  a field-level error on blur.


  That said, it’s a good idea to always validate on the server side even if you
  use client-side validation for formatting checks. That’s because JavaScript
  validation may not work on all clients; JavaScript errors could occur no
  matter the client; and JS validation can easily be bypassed, which raises
  security concerns.


  In general, the best practice for server-side validation is to mark errors
  with both form-level and field-level errors.


  #### Accessibility


  For screen reader accessibility, form-level errors should include anchor links
  to the problem field in question. In general, use distinct icons, contrasting
  colors, prominent placement, and text to indicate errors. Don’t rely on just
  one method, as users can have many different accessibility needs (color blind
  users, visually impaired users, users with motor control issues, etc.).


  ### States


  #### Action


  The action notification displays when something is happening on the page, such
  as a page loading notification as search results are found. Use animated
  minicons to reassure the user that an action is functioning as intended.


  * Border: 1 px, Gray 40 (#b4b5b6)

  * Background: Gray 10 (#f7f8f9)

  * Padding: 15px

  * H4 (Avenir Next Medium, 18 px) Black (#101820)

  * Minicon: 18 px, Gray (#5a5d61)


  #### Success


  The success notification displays when an operation has run as expected, such
  as returning the number of results in a search or a form has been successfully
  submitted.


  * Border: 2 px, CFPB Green (#20aa3f)

  * Background: Green 20 (#e2efd8)

  * Minicon: 18px, CFPB Green (#20aa3f)


  #### Success (field-level)


  * Border: 2 px, CFPB Green (#20aa3f)

  * Minicon: 18 px, CFPB Green (#20aa3f)

  * Success minicon and message should always appear below input field


  #### Warning


  The warning notification displays when an operation has run as expected, but
  doesn’t have the expected results,such as a search that returned no
  results.This can also be used to display additional critical information to a
  user before they submit a form, such as how their data will be used and
  protected or a reminder that they can’t edit their responses after submitting.


  * Border: 2 px, Gold (#ff9e1b)

  * Background: Gold 20 (#fff0dd)

  * Minicon: 18px, Gold (#ff9e1b)


  #### Warning (field-level)


  * Border: 2 px, Gold (#ff9e1b)

  * Minicon: 18 px, Gold (#ff9e1b)


  #### Error


  The error notification displays when an operation has not run as expected and
  encounters an error. Use after validating on the server side to call out input
  errors preventing form submission.


  For screen reader accessibility, include anchor links to the fields that need
  correction


  * Place form-level alerts below the form title

  * Border: 2 px, Red (#d14124)

  * Background: Red 20 (#fff0dd)

  * Minicon: 18px, Red (#d14124)


  #### Error (field-level)


  * Border: 2 px, Red (#d14124)

  * Minicon: 18 px, Red (#d14124)

  * Error minicon and message should always appear below input field
html-snippet: >-
  <div class="m-notification             m-notification__visible">     {%
  include icons/information-round.svg %}     <div
  class="m-notification_content">         <div class="h4
  m-notification_message">A default notification</div>     </div> </div>
jinja2-snippet: >-
  <div class="m-notification             m-notification__visible">     {%
  include icons/information-round.svg %}     <div
  class="m-notification_content">         <div class="h4
  m-notification_message">A default notification</div>     </div> </div>
section: []
---

