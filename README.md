[![GitHub version](https://badge.fury.io/gh/motss%2Fpaper-swipe.svg)](http://badge.fury.io/gh/motss%2Fpaper-swipe)
[![Bower version](https://badge.fury.io/bo/paper-swipe.svg)](http://badge.fury.io/bo/paper-swipe)

# paper-swipe

See the [component page](http://motss.github.io/paper-swipe/components/paper-swipe/) for more information.

`paper-swipe` provides enables swipe gestures to swipe content to either the left or the right to unveil the underlay
behind it.

Example:

    <paper-swipe>By default, it can be swiped to either the left or the right.</paper-swipe>
    <paper-swipe disable-swipe>Swipe Gestures disabled</paper-swipe>
    <paper-swipe fade>Swipe with fade in/ fade out effect</paper-swipe>
    <paper-swipe left-swipe>Only Left Swipe</paper-swipe>
    <paper-swipe right-swipe>Only Right Swipe</paper-swipe>
    <paper-swipe on-tap-underlay='tapHandler'>Tap Event Handler</paper-swipe>
    <paper-swipe on-edge='edgeHandler'>Panel is now at the edge of the screen</paper-swipe>

`paper-swipe` allows user to use the custom DOM in the body to create basically any contents and it has two different
sections which allows the customization by using the `content` and `underlay` attributes:

Example:

    <paper-swipe>
      <div underlay>Underlay content goes here...</div>
      <div content>Content of swiping element goes here...</div>
    </paper-swipe>

## Event handling

`paper-swipe` has been added some features to fire certain events such as `tap-underlay` and `edge` so that user can
make use of it to perform additional functions as you like:

Example:

    <paper-swipe on-edge="edgeHandler"
      <div underlay>Underlay content goes here...</div>
      <div content>Fire `edge` event when the panel is at the edge of the screen...</div>
    </paper-swipe>

    <paper-swipe on-tap-underlay="tapHandler">
      <div underlay>Underlay content goes here...</div>
      <div content>Fire `tap-underlay` event when the panel is being clicked...</div>
    </paper-swipe>

There are two ways to disable the swiping on the content panel by using `on-tap-underlay` or `on-click` event handler:

Example:

    <paper-swipe on-edge="resetPanel" on-tap-underlay="disablePanel">
        <div underlay>Click to reset the panel from the edge to its origin...</div>
        <div content>Swipe to remove the panel...</div>
    </paper-swipe>

    <paper-swipe on-edge="resetPanel">
        <div underlay on-click="disablePanel">Click to reset the panel from the edge to its origin...</div>
        <div content>Swipe to remove the panel...</div>
    </paper-swipe>

## Styling
Note, it's important that specifying explicit height to the `paper-swipe` will render both the `content` and `underlay` layers to have the same height. Especially when multiple `paper-swipe` on the same document, explicit height will make all elements look consistent.

    paper-swipe {
      height: 100px;
    }

    paper-swipe {
      --paper-swipe: {
        height: 100px;
      };
    }

The following custom properties and mixins are also available for styling:

Custom mixin | Description | Default
----------------|-------------|----------
`--paper-swipe` | `Mixin applied to paper-swipe` | `{}`
`--paper-swipe-swipeable-container` | `Mixin applied to paper-swipe-swipeable-container` | `{}`
`--paper-swipe-content` | `Mixin applied to swipeable content` | `{}`
`--paper-swipe-underlay` | `Mixin applied to underlay beneath the swipeable content` | `{}`

## Demo + boilerplate generator
[paper-swipe demo + boilerplate generator](http://motss.github.io/paper-swipe/components/paper-swipe/demo/index.html)

## Getting Started

1. Install with bower  
`bower install --save paper-swipe`

2. Load the web component and the dependencies

```html
<script src="/path-to-bower-components/webcomponentsjs/webcomponents-lite.min.js"></script>
<link rel="import" href="/path-to-bower-components/polymer/polymer.html">
<link rel="import" href="/path-to-bower-components/paper-swipe/paper-swipe.html">
```

3. Markup with &lt;paper-swipe&gt;&lt;/paper-swipe&gt;

4. Done

### Supported Browsers

[Same as Polymer](http://www.polymer-project.org/resources/compatibility.html)
