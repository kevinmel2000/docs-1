Class **Phalcon\\Validation\\Validator\\Between**
=================================================

*extends* abstract class :doc:`Phalcon\\Validation\\Validator <Phalcon_Validation_Validator>`

*implements* :doc:`Phalcon\\Validation\\ValidatorInterface <Phalcon_Validation_ValidatorInterface>`

.. role:: raw-html(raw)
   :format: html

:raw-html:`<a href="https://github.com/phalcon/cphalcon/blob/master/phalcon/validation/validator/between.zep" class="btn btn-default btn-sm">Source on GitHub</a>`

Validates that a value is between an inclusive range of two values. For a value x, the test is passed if minimum<=x<=maximum.  

.. code-block:: php

    <?php

     use Phalcon\Validation\Validator\Between;
    
     $validator->add('price', new Between([
         'minimum' => 0,
         'maximum' => 100,
         'message' => 'The price must be between 0 and 100'
     ]));
    
     $validator->add(['price', 'amount'], new Between([
         'minimum' => [
             'price' => 0,
             'amount' => 0
         ],
         'maximum' => [
             'price' => 100,
             'amount' => 50
         ],
         'message' => [
             'price' => 'The price must be between 0 and 100',
             'amount' => 'The amount must be between 0 and 50'
         ]
     ]));



Methods
-------

public  **validate** (:doc:`Phalcon\\Validation <Phalcon_Validation>` $validation, *mixed* $field)

Executes the validation



public  **__construct** ([*array* $options]) inherited from Phalcon\\Validation\\Validator

Phalcon\\Validation\\Validator constructor



public  **isSetOption** (*mixed* $key) inherited from Phalcon\\Validation\\Validator

Checks if an option has been defined



public  **hasOption** (*mixed* $key) inherited from Phalcon\\Validation\\Validator

Checks if an option is defined



public  **getOption** (*mixed* $key, [*mixed* $defaultValue]) inherited from Phalcon\\Validation\\Validator

Returns an option in the validator's options Returns null if the option hasn't set



public  **setOption** (*mixed* $key, *mixed* $value) inherited from Phalcon\\Validation\\Validator

Sets an option in the validator



