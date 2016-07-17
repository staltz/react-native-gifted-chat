# Gifted Messenger
The most complete chat UI for React Native

# Installation
- `npm install react-native-gifted-messenger --save`

# Simple example
```javascript
import React, { Component } from 'react';
import {GiftedMessenger} from 'react-native-gifted-messenger';

export default class Example extends Component {
  constructor(props) {
    super(props);
    this.state = {messages: []};
    this.onSend = this.onSend.bind(this);
  }
  componentWillMount() {
    this.setState({
      messages: [
        {
          _id: 1,
          text: 'Hello developer',
          createdAt: new Date(Date.UTC(2016, 5, 11, 17, 10, 0)),
          user: {
            _id: 2,
            name: 'React Native',
            avatar: 'https://facebook.github.io/react/img/logo_og.png',
          },
        },
      ],
    });
  }
  onSend(messages = []) {
    this.setState((previousState) => {
      return {
        ...previousState,
        messages: GiftedMessenger.append(previousState.messages, messages),
      };
    });
  }
  render() {
    return (
      <GiftedMessenger
        messages={this.state.messages}
        onSend={this.onSend}
        user={{
          _id: 1,
        }}
      />
    );
  }
}
```

# Advanced example
See [example project](example/Example.js)

# Props

# Components
## Actions
- **Rendered by default** - No

### Props
- **options**
- **icon**
- **containerStyle**
- **iconStyle**

## Avatar
## Bubble
## ParsedText
## BubbleImage
## Composer (might be renamed)
## CustomView
## Day
## InputToolbar
## Loading
## Location (deprecated)
## Message
## Send
## Time


# LICENSE
- [MIT](LICENSE)