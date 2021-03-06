.. include:: Images.txt

.. ==================================================
.. FOR YOUR INFORMATION
.. --------------------------------------------------
.. -*- coding: utf-8 -*- with BOM.

.. ==================================================
.. DEFINE SOME TEXTROLES
.. --------------------------------------------------
.. role::   underline
.. role::   typoscript(code)
.. role::   ts(typoscript)
   :class:  typoscript
.. role::   php(code)


.. _select:

Selectfield
~~~~~~~~~~~

What does it do?
''''''''''''''''

- **General:** A select field is also called "dropdown", "combobox" or "picklist". The user can choose an option. It's also possible to config a multiselectfield - the user can choose more than only one option by holding the CRTL-Key when clicking a second option. Add some options and separate it with a new line.
- **Mandatory:** This field could be marked as mandatory, so the user must fill out this field, otherwise the form can not be submitted.
- **Prefill:** The field can be preselected from FlexForm, TypoScript, GET/Post-Params or from FE_User table.
- **Special:** Options could also filled by TypoScript in powermail 2.1 and higher (static or dynamic)

Frontend Output Example
'''''''''''''''''''''''

|img-33|

Backend Configuration Example
'''''''''''''''''''''''''''''

|img-34|

|img-35|

Explanation
'''''''''''

.. t3-field-list-table::
 :header-rows: 1

 - :Field:
      Field
   :Description:
     Description
   :Explanation:
      Explanation
   :Tab:
      Tab

 - :Field:
      Title
   :Description:
      Add a label for this field.
   :Explanation:
      The label is shown in the frontend near to this field.
   :Tab:
      General

 - :Field:
      Type
   :Description:
      Choose a fieldtype.
   :Explanation:
      See explanation below for a special fieldtype. Different fields are related to some fieldtypes – not all fields are shown on every type.
   :Tab:
      General

 - :Field:
      Options
   :Description:
      Options to select
   :Explanation:
      Separate each with a new line. **Note: see following
      table for examples, how to preselect or clean a value**
   :Tab:
      General

 - :Field:
      Email of sender
   :Description:
      Check this if this field contains the email of the sender.
   :Explanation:
      This is needed to set the correct sender-email-address. If there is no field marked as Senderemail within the current form, powermail will use a default value for the Senderemail.
   :Tab:
      General

 - :Field:
      Name of sender
   :Description:
      Check this if this field contains the name (or a part of the name) of the sender.
   :Explanation:
      This is needed to set the correct sender-name. If there is no field marked as Sendername within the current form, powermail will use a default value for the Sendername.
   :Tab:
      General

 - :Field:
      Mandatory Field
   :Description:
      This field must contain input.
   :Explanation:
      Check this if the field must contain input, otherwise submitting the form is not possible.
   :Tab:
      Extended

 - :Field:
      Value from logged in Frontend User
   :Description:
      Check if field should be filled from the FE_Users table of a logged in fe_user.
   :Explanation:
      This value overwrites a static value, if set.
   :Tab:
      Extended

 - :Field:
      Create from TypoScript
   :Description:
      Fill Options from TypoScript
   :Explanation:
      If you want to create your options (see above) from TypoScript, you can use this field. Please split each line in your TypoScript with [\\n]


      Example:

      lib.options = TEXT

      lib.options.value = red[\\n]blue[\\n]pink
   :Tab:
     Extended

 - :Field:
      Layout
   :Description:
      Choose a layout.
   :Explanation:
      This adds a CSS-Class to the frontend output. Administrator can add, remove or rename some of the entries.
   :Tab:
      Extended

 - :Field:
      Description
   :Description:
      Add a description for this field.
   :Explanation:
      Per default a description will be rendered as title-attribute in the labels in frontend.
   :Tab:
      Extended

 - :Field:
      Multiselect
   :Description:
      Choose a layout.
   :Explanation:
      This adds a CSS-Class to the frontend output. Administrator can add, remove or rename some of the entries.
   :Tab:
      Extended

 - :Field:
      Variables – Individual Fieldname
   :Description:
      This is a marker of this field.
   :Explanation:
      Use a field variable with {marker} in any RTE or HTML-Template. The marker name is equal in any language.
   :Tab:
      Extended

 - :Field:
      Add own Variable
   :Description:
      Check this, if you want to set your own marker (see row before).
   :Explanation:
      After checking this button, TYPO3 ask you to reload. After a reload, you see a new field for setting an own marker.
   :Tab:
      Extended

 - :Field:
      Language
   :Description:
      Choose a language.
   :Explanation:
      Choose in which frontend language this record should be rendered.
   :Tab:
      Access

 - :Field:
      Hide
   :Description:
      Disable the form
   :Explanation:
      Enable or disable this record.
   :Tab:
      Access

 - :Field:
      Start
   :Description:
      Startdate for this record.
   :Explanation:
      Same function as known from default content elements or pages in TYPO3.
   :Tab:
      Access

 - :Field:
      Stop
   :Description:
      Stopdate for this record.
   :Explanation:
      Same function as known from default content elements or pages in TYPO3.
   :Tab:
      Access


Option examples for selectbox
'''''''''''''''''''''''''''''

.. t3-field-list-table::
 :header-rows: 1

 - :Example:
     Example option
   :HTML:
     Generated HTML code in Frontend

 - :Example:
      Red
   :HTML:
      <option value=”Red”>Red</option>

 - :Example:
      Yellow \| 1
   :HTML:
      <option value=”1”>Yellow</option>

 - :Example:
      Blue \|
   :HTML:
      <option value=””>Blue</option>

 - :Example:
      Black Shoes \| black \| \*
   :HTML:
      <option value=”black” selected=”selected”>Black Shoes</option>

 - :Example:
      White \| \| \*
   :HTML:
      <option value=”” selected=”selected”>White</option>

 - :Example:
      Please choose... \|
      | red
      | blue
   :HTML:
      | <option value=””>Please choose...</option>
      | <option>red</option>
      | <option>blue</option>

