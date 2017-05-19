# Your snippets
#
# Atom snippets allow you to enter a simple prefix in the editor and hit tab to
# expand the prefix into a larger code block with templated values.
#
# You can create a new snippet in this file by typing "snip" and then hitting
# tab.
#
# An example CoffeeScript snippet to expand log to console.log:
#
# '.source.coffee':
#   'Console log':
#     'prefix': 'log'
#     'body': 'console.log $1'
#
# Each scope (e.g. '.source.coffee' above) can only be declared once.
#
# This file uses CoffeeScript Object Notation (CSON).
# If you are unfamiliar with CSON, you can read more about it in the
# Atom Flight Manual:
# http://flight-manual.atom.io/using-atom/sections/basic-customization/#_cson


'.source.js.jsx':
  'React Statless Function':
    'prefix': 'rsf'
    'body': """
      import React from 'react';

      const $1 = (props) => (
        <div></div>;
      );

      export default $1;
    """

  'React Class Component':
    'prefix': 'rcc'
    'body': """
      import React, { Component } from 'react';

      class $1 extends Component {
        constructor(props) {
          super(props);
        }

        render() {
          return (
            <div></div>
          );
        }
      }

      export default $1;
    """

  'React Container Component':
    'prefix': 'rcontainer',
    'body': """
      import React, { Component} from 'react';
      import { connect} from 'react-redux';
      import { bindActionCreators } from 'redux';

      class $1 extends Component {
        constructor(props) {
          super(props);
        }

        render() {
          return <div></div>
        }
      }

      function mapDispatchToProps(dispatch) {
        return bindActionCreators({}, dispatch);
      }

      export default connect(null, mapDispatchToProps)($1);
    """

  'Switch Statement':
    'prefix': 'switch'
    'body': """
      switch (expression) {
      case expression:

      default:

      }
    """

  'Import':
    'prefix': 'import'
    'body': """
      import $1 from '$1';
    """

  'Bind this':
      'prefix': 'bthis'
      'body': """
      this.$1 = this.$1.bind(this);
      """

  'Reducer':
    'prefix': 'red'
    'body': """
    import { TYPE } from '../actions/types';

    const INITIAL_STATE = {};

    export default (state = INITIAL_STATE, action) => {
      switch (action.type) {
      case 'ACTION_TYPE':
        return action.payload;
      default:
        return state;
      }
    };
    """
