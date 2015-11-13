# Messages

A message can contain one or more elements!

{% patch %}porres_examples/Messages_1.pd{% endpatch %}

In Pure Data, all of the Data is received and sent in form of Messages. An atom is an element in a message, and the elements can only be NUMBERS or SYMBOLS. Patches are a net of Data Flow! Objetcs receive and send messages.

{% patch %}porres_examples/Messages_2.pd{% endpatch %}

When we click on a Message Box, what's in it is sent throughout its outlet. Click on these messages and check Pd's Terminal window.

Messages can also be interpreted as specific commands. The most important command is the "bang" Message. We'll see that later!

{% patch %}porres_examples/Messages_3.pd{% endpatch %}

In a Message Box, we can also have more than one message. To separate messages we need to put a comma in between them.

{% patch %}porres_examples/Messages_4.pd{% endpatch %}

Another thing is that when a message receives something on its inlet, it is activated and sends out the message it contains.

{% patch %}porres_examples/Messages_5.pd{% endpatch %}

