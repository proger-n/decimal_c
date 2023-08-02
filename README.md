# decimal_c
Native implementation of the decimal.h library in C

## Information

The Decimal value type represents decimal numbers ranging from positive 79,228,162,514,264,337,593,543,950,335 to negative 79,228,162,514,264,337,593,543,950,335. The Decimal value type is appropriate for financial calculations that require large numbers of significant integral and fractional digits and no round-off errors. The Decimal type does not eliminate the need for rounding. Rather, it minimizes errors due to rounding.


### Arithmetic Operators

| Operator name | Operators  | Function                                                                           | 
| ------ | ------ |------------------------------------------------------------------------------------|
| Addition | + | s21_add(s21_decimal value_1, s21_decimal value_2, s21_decimal *result)         |
| Subtraction | - | s21_sub(s21_decimal value_1, s21_decimal value_2, s21_decimal *result) |
| Multiplication | * | s21_mul(s21_decimal value_1, s21_decimal value_2, s21_decimal *result) | 
| Division | / | s21_div(s21_decimal value_1, s21_decimal value_2, s21_decimal *result) |


### Comparison Operators

| Operator name | Operators  | Function | 
| ------ | ------ | ------ |
| Less than | < | s21_is_less(s21_decimal, s21_decimal) |
| Less than or equal to | <= | s21_is_less_or_equal(s21_decimal, s21_decimal) | 
| Greater than | > |  s21_is_greater(s21_decimal, s21_decimal) |
| Greater than or equal to | >= | s21_is_greater_or_equal(s21_decimal, s21_decimal) | 
| Equal to | == |  s21_is_equal(s21_decimal, s21_decimal) |
| Not equal to | != |  s21_is_not_equal(s21_decimal, s21_decimal) |


### Convertors and parsers

| Convertor/parser | Function | 
| ------ | ------ |
| From  | s21_from_int_to_decimal(src, s21_decimal *dst) |
| From float  | s21_from_float_to_decimal(float src, s21_decimal *dst) |
| To  | s21_from_decimal_to_int(s21_decimal src, *dst) |
| To float  | s21_from_decimal_to_float(s21_decimal src, float *dst) |


### Another functions

| Description | Function                                                         | 
| ------ |------------------------------------------------------------------|
| Rounds a specified Decimal number to the closest integer toward negative infinity. | s21_floor(s21_decimal value, s21_decimal *result)            |	
| Rounds a decimal value to the nearest integer. | s21_round(s21_decimal value, s21_decimal *result)    |
| Returns the integral digits of the specified Decimal; any fractional digits are discarded, including trailing zeroes. | s21_truncate(s21_decimal value, s21_decimal *result) |
| Returns the result of multiplying the specified Decimal value by negative one. | s21_negate(s21_decimal value, s21_decimal *result)   |