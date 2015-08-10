# paper-swipe

See the [component page](http://motss.github.io/paper-swipe/components/paper-swipe/) for more information.

`paper-swipe` provides enables swipe gestures to swipe content to either the left or the right to unveil the underlay
behind it.

Example:

    <paper-swipe disable-swipe>Swipe Gestures disabled</paper-swipe>
    <paper-swipe reset-swipe>Reset panel position</paper-swipe>
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

### Event handling

`paper-swipe` has been added some features to fire certain events such as `tap-underlay` and `edge` so that user can
make use of it to perform additional functions as you like:

Example:

    <paper-swipe on-edge="edgeHandler">
      <div underlay>Underlay content goes here...</div>
      <div content>Fire `edge` event when the panel is at the edge of the screen...</div>
    </paper-swipe>

    <paper-swipe on-tap-underlay="tapHandler">
      <div underlay>Underlay content goes here...</div>
      <div content>Fire `tap-underlay` event when the panel is being clicked...</div>
    </paper-swipe>

`reset-swipe' attribute has been added as new feature to tell the user that the swiping panel has to return to its
origin and it is usually used with `on-edge` event handler to perform the additional task:

Example:

    <paper-swipe on-edge="resetPanel">
        <div underlay>Click to reset the panel from the edge to its origin...</div>
        <div content>Swipe to remove the panel...</div>
    </paper-swipe>

## Demo
[http://motss.github.io/paper-swipe/components/paper-swipe/demo/index.html](http://motss.github.io/paper-swipe/components/paper-swipe/demo/index.html)

### Attributes
<table>
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<th>swipeLeft</th>
<td>boolean</td>
<td>false</td>
<td>If true, only swiping to the left.</td>
</tr>
<tr>
<th>swipeRight</th>
<td>boolean</td>
<td>false</td>
<td>If true, only swiping to the right.</td>
</tr>
<tr>
<th>disableSwipe</th>
<td>boolean</td>
<td>false</td>
<td>If true, swiping is disabled.</td>
</tr>
<tr>
<th>resetSwipe</th>
<td>boolean</td>
<td>false</td>
<td>If true, the panel will return to its origin.</td>
</tr>
<tr>
<th>peekOffset</th>
<td>number</td>
<td>30</td>
<td>How many pixels on the side of the screen appears.</td>
</tr>
<tr>
<th>slideOffset</th>
<td>number</td>
<td>80</td>
<td>How many pixels needed to trigger auto-slide to the edge.</td>
</tr>
</tbody>
</table>

## Getting Started

1. Install with bower  
`bower install --save paper-swipe`

2. Load the web component and the dependencies

```html
<script src="bower_components/webcomponentsjs/webcomponents.js"></script>
<link rel="import" href="bower_components/polymer/polymer.html">
<link rel="import" href="bower_components/paper-swipe/paper-swipe.html">
```

3. Markup with &lt;paper-swipe&gt;

4. Done

### Supported Browsers

[Same as Polymer](http://www.polymer-project.org/resources/compatibility.html)
