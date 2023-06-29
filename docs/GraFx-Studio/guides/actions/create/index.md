# How to create an Action

!!! example "Experimental"
    Actions are released as Experimental.
    This means that you can use them to test out future functionality, but the actual implementation is not final yet.

## Add Action

Open the [Automation panel](GraFx-Studio/overview/properties/#automation-properties).

By default, a new document will not have any Actions.

You can add an Action using the "+" sign or edit existing ones with the pencil icon.

![screenshot](actionlist.png)

## Define Triggers for the Action

In the Action, first select a Trigger - an event that will kick off the Action.

![screenshot](trigger.png)

If applicable, select the scope for the Trigger.

The scope is the object (frame, variable, etc.) that will be monitored. You can also choose to monitor "Any variable" or "Any frame".

![screenshot](triggerscope.png)

What Triggers are available?

### Select Layout changed

The chosen layout is changed.

![screenshot](layouts.png)

### Frame moved

When the position (or size) of a frame changes.

This Trigger is detected when the X, Y, width, height, or rotation changes.

![screenshot](framelocation.png)

### Page size changed

This Trigger is detected only in the Studio UI. In the Studio UI, an end-user can set the page size. This page size will determine the closest fitting layout.

This Trigger will detect the page size change and execute the Actions.

### Document loaded

Triggered when the document is loaded on the canvas.

### Variable value changed

Triggered when the value of a variable is changed.

Imagine a change in name or price. This change can be triggered by an end-user or through the population of variable data via datasources.

## Write JavaScript to be executed

Click on the "Action" tab to start writing your script.

The example below reads the value of the variable "reduction" and translates it into a string of characters.

If the value is "promo", then the position of the frame (shape: "promoPop") behind the price will be offset outside the page or returned to the actual position.

![screenshot](action.png)

![screenshot](promoYes.png)

![screenshot](promoNo.png)