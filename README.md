# Buttons - React Basics

A React Basics Buttons component. Stateless, fully optimized with css animations, highly customizable and Mobile support.

## Installation

Into your project's root directory run the following command:


**npm**
```console
npm i -P rb-buttons
```

**Yarn**
```console
yarn add rb-buttons
```

This package only has 1 dependencies:

- `react@16.2.0`

## Example

Buttons is one of the components inside React Basics, so if you want test it, go https://edgravill.github.io/react-basics and see it working.

> The website is under construction

## Usage

Component constantly changes its width, so it's recommendable put inside div container to control its position.

```javascript
import React from 'react';
import Button from 'rb-buttons';

const Index = ({
  fetching,
  sendComment,
}) => (
  <div>
    <textarea id="comment" />
    <div className="buttonContainer">
      <Button
        active={!fetching}
        loading={fetching}
        onClick={() => sendComment(document.getElementById('comment'))}
        text="Enviar"
      />
    </div>
  </div>
);
```

## API

|Prop|Required|Type|Default|Description|
|----|--------|----|-------|-----------|
|active|`false`|`boolean`|`true`|Prop who determines if button catch click action.|
|loaded|`false`|`boolean`|`false`|Prop who determines if loading finish.|
|loadedStyle|`false`|`Object`|`{}`|Button style when "loaded" prop is `true`.|
|loadedText|`false`|`string`|`''`|Text to display in button when "loaded" prop is `true`. Only works in `'filler'` or `'text'` loading type.|
|loading|`false`|`boolean or number`|`false`|Prop who determines if loading animation start. If loading type is `'filler'` this prop also take a number between 0 an 1 to handle loading %.|
|loadingStyle|`false`|`Object`|`{}`|Button style when "loading" prop is `true`.|
|loadingText|`false`|`string`|`''`|Text to display in button when "loading" prop is `true`. Only works in `'filler'` or `'text'` loading type.|
|loadingType|`false`|`Enum: 'spinner', 'textSpinner', 'filler', 'text'`|`'spinner'`|Type of loading animation. See [Loading Types description below](#loadingTypes).|
|onClick|`true`|`Function`|`undefined`|Function to perform when user click the button.|
|style|`false`|`Object`|`{}`|Style of the button when is normal.|
|text|`true`|`string`|`undefined`|Default text to display in the button. If "loadedText" or "loadingText" props are undefined or empty this text will be displayed.|

### loadingTypes

#### spinner

The buttom becomes in a spinner circle

#### textSpinner

The buttom keep its shape, but the text becomes in a spinner circle

#### filler

Alfa white layer fill the buttom

#### text

There is no animation, only changes the display text if is loading and when is loaded

## Goals

- [ ] Integration with icons (Under develop)

> looking for more? - Do a pull request with your proposals ;)

## Collaborators

- Eduardo Grajales Villanueva @EdGraVill

> If you want to collaborate with this or another exist or new component inside React Basics, first do a pull request and then email me: edgravill@gmail.com

If you want pull request some changes, don't forget build it firt with the following command:

**npm**
```console
npm run build
```

**Yarn**
```console
yarn build
```

Once you're a collaborator don't forget 3 rules:

1. Version are `Mayor` (If APIs are deleted or create new one) `.` `Medium` (If APIs changes without changing name) `.` `Minimum` (If do some hotfix, change Documentation or develop configurations). This is because all 1.x.x are compatible, but are incompatible with 2.x.x
2. Build a great components and do the best documentation as you can.
3. Share with your developer friends. It would be useful for them.

Don't forget [join discussion on Slack](https://join.slack.com/t/react-basics/shared_invite/enQtMzM4MDMyNzM5NjgxLTMxYzcwMDMwYmNkZGIxNWFkZGZhMDVmNWU3OTQ3ZDhlYmZhOWU0NTkwMTdkNzg5ZTJhNWE3MDJlNTc3OGU4YjA)

## Licence

MIT License

Copyright (c) 2018 Eduardo Grajales Villanueva

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
