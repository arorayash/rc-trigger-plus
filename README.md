# rc-trigger-plus

---

This trigger component added custom functionality to React Trigger Component

v1.1.1

## Browser Support

| IE 8+ ✔ | Chrome 31.0+ ✔ | Firefox 31.0+ ✔ | Opera 30.0+ ✔ | Safari 7.0+ ✔ |

## Development

```
npm install
npm start
```

## Example

http://localhost:8200/examples/

## Feature

- supported on IE 8+, Chrome, Firefox, and Safari

## Usage

Include the default
[styling](https://github.com/react-component/trigger/blob/master/assets/index.less#L4:L11)
and then:

```js
import React from "react";
import ReactDOM from "react-dom";
import Trigger from "rc-trigger-plus";

ReactDOM.render(
	<Trigger
		action={["click"]}
		popup={<span>popup</span>}
		popupAlign={{
			points: ["tl", "bl"],
			offset: [0, 3]
		}}
	>
		<a href="#">hover</a>
	</Trigger>,
	container
);
```

## API

### props

<table class="table table-bordered table-striped">
    <thead>
    <tr>
        <th style="width: 100px;">name</th>
        <th style="width: 50px;">type</th>
        <th style="width: 50px;">default</th>
        <th>description</th>
    </tr>
    </thead>
    <tbody>
        <tr>
          <td>alignPoint</td>
          <td>bool</td>
          <td>false</td>
          <td>Popup will align with mouse position (support action of 'click', 'hover' and 'contextMenu')</td>
        </tr>
        <tr>
          <td>popupClassName</td>
          <td>string</td>
          <td></td>
          <td>additional className added to popup</td>
        </tr>
        <tr>
          <td>forceRender</td>
          <td>boolean</td>
          <td>false</td>
          <td>whether render popup before first show</td>
        </tr>
        <tr>
          <td>destroyPopupOnHide</td>
          <td>boolean</td>
          <td>false</td>
          <td>whether destroy popup when hide</td>
        </tr>
        <tr>
          <td>getPopupClassNameFromAlign</td>
          <td>getPopupClassNameFromAlign(align: Object):String</td>
          <td></td>
          <td>additional className added to popup according to align</td>
        </tr>
        <tr>
          <td>action</td>
          <td>string[]</td>
          <td>['hover']</td>
          <td>which actions cause popup shown. enum of 'hover','click','focus','contextMenu'</td>
        </tr>
        <tr>
          <td>mouseEnterDelay</td>
          <td>number</td>
          <td>0</td>
          <td>delay time to show when mouse enter. unit: s.</td>
        </tr>
        <tr>
          <td>mouseLeaveDelay</td>
          <td>number</td>
          <td>0.1</td>
          <td>delay time to hide when mouse leave. unit: s.</td>
        </tr>
        <tr>
          <td>popupStyle</td>
          <td>Object</td>
          <td></td>
          <td>additional style of popup</td>
        </tr>
        <tr>
          <td>prefixCls</td>
          <td>String</td>
          <td>rc-trigger-popup</td>
          <td>prefix class name</td>
        </tr>
        <tr>
          <td>popupTransitionName</td>
          <td>String|Object</td>
          <td></td>
          <td>https://github.com/react-component/animate</td>
        </tr>
        <tr>
          <td>maskTransitionName</td>
          <td>String|Object</td>
          <td></td>
          <td>https://github.com/react-component/animate</td>
        </tr>
        <tr>
          <td>onPopupVisibleChange</td>
          <td>Function</td>
          <td></td>
          <td>call when popup visible is changed</td>
        </tr>
        <tr>
          <td>mask</td>
          <td>boolean</td>
          <td>false</td>
          <td>whether to support mask</td>
        </tr>
        <tr>
          <td>maskClosable</td>
          <td>boolean</td>
          <td>true</td>
          <td>whether to support click mask to hide</td>
        </tr>
        <tr>
          <td>popupVisible</td>
          <td>boolean</td>
          <td></td>
          <td>whether popup is visible</td>
        </tr>
        <tr>
          <td>zIndex</td>
          <td>number</td>
          <td></td>
          <td>popup's zIndex</td>
        </tr>
        <tr>
          <td>defaultPopupVisible</td>
          <td>boolean</td>
          <td></td>
          <td>whether popup is visible initially</td>
        </tr>
        <tr>
          <td>popupAlign</td>
          <td>Object: alignConfig of [dom-align](https://github.com/yiminghe/dom-align)</td>
          <td></td>
          <td>popup 's align config</td>
        </tr>
        <tr>
          <td>onPopupAlign</td>
          <td>function(popupDomNode, align)</td>
          <td></td>
          <td>callback when popup node is aligned</td>
        </tr>
        <tr>
          <td>popup</td>
          <td>React.Element | function() => React.Element</td>
          <td></td>
          <td>popup content</td>
        </tr>
        <tr>
          <td>getPopupContainer</td>
          <td>getPopupContainer(): HTMLElement</td>
          <td></td>
          <td>function returning html node which will act as popup container</td>
        </tr>
        <tr>
          <td>getDocument</td>
          <td>getDocument(): HTMLElement</td>
          <td></td>
          <td>function returning document node which will be attached click event to close trigger</td>
        </tr>
        <tr>
          <td>popupPlacement</td>
          <td>string</td>
          <td></td>
          <td>use preset popup align config from builtinPlacements, can be merged by popupAlign prop</td>
        </tr>
        <tr>
          <td>builtinPlacements</td>
          <td>object</td>
          <td></td>
          <td>builtin placement align map. used by placement prop</td>
        </tr>
        <tr>
          <td>stretch</td>
          <td>string</td>
          <td></td>
          <td>Let popup div stretch with trigger element. enums of 'width', 'minWidth', 'height', 'minHeight'. (You can also mixed with 'height minWidth')</td>
        </tr>
        <tr>
          <td>ignoreVisibilityChangeClassName</td>
          <td>string</td>
          <td></td>
          <td>Ignore the pop visibility change to false when the target has the `ignoreVisibilityChangeClassName`</td>
        </tr>
    </tbody>
</table>

## Test Case

```
npm test
npm run chrome-test
```

## Coverage

```
npm run coverage
```

open coverage/ dir

## React 16 Note

After React 16, you won't access popup element's ref in parent component's
componentDidMount, which means following code won't work.

```javascript
class App extends React.Component {
	componentDidMount() {
		this.input.focus(); // error, this.input is undefined.
	}

	render() {
		return (
			<Trigger
				action={["click"]}
				popup={
					<div>
						<input ref={node => (this.input = node)} type="text" />
					</div>
				}
			>
				<button>click</button>
			</Trigger>
		);
	}
}
```

Consider wrap your popup element to a separate component:

```javascript
class InputPopup extends React.Component {
	componentDidMount() {
		this.props.onMount();
	}

	render() {
		return (
			<div>
				<input ref={this.props.inputRef} type="text" />
			</div>
		);
	}
}

class App extends React.Component {
	handlePopupMount() {
		this.input.focus(); // error, this.input is undefined.
	}

	render() {
		return (
			<Trigger
				action={["click"]}
				popup={
					<InputPopup
						inputRef={node => (this.input = node)}
						onMount={this.handlePopupMount}
					/>
				}
			>
				<button>click</button>
			</Trigger>
		);
	}
}
```

## License

rc-trigger-plus is released under the MIT license.
