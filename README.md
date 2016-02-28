# decimal-behavior

A decimal-behavior element that provides ceil, round, floor, format and decimalAdjustemnt methods. 
Decimal adjustment of a number implementation is taken from Mozilla Developer Network: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/round.


## Installation
Install using bower

    bower i decimal-behavior -S

Import the behavior

    <link rel="import" href="../bower_components/decimal-behavior/decimal-behavior.html">

Inlude the behavior in your web component

    behaviors: [DecimalBehavior]

## Example

    <link rel="import" href="../decimal-behavior.html">
    <dom-module id="x-decimal-behavior">
      <template>
        <style>
          :host {
            display: inline-block;
          }
        </style>
        <h1>decimal-behavior</h1>
        <div>[[formatNumber(3.125, 2)]]</div>            // Result: 3.13
        <div>[[formatNumber(3.1415, 3, 'floor')]]</div>  // Result: 3.141
        <div>[[formatNumber(3.14151, 4, 'ceil')]]</div>  // Result: 3.1416
      </template>
      <script>
        Polymer({
          is: 'x-decimal-behavior',
          behaviors: [DecimalBehavior]
        });
      </script>
    </dom-module>

