D. Keith Casey
The API guide book
[book website](http://theapidesignbook.com)

### Goals

1. Build something useful
2. Go home.

### Documentation

[Slate](https://github.com/lord/slate) is a great documentation

[Open Api (used to be swagger)](http://docs.clarify.io/api/)

First thing to do in documentation: authentication

# DO NOT

- Create your own HTTP verbs.
- CREATE YOUR OWN RESPONSE CODES
- Create your own encryption scheme
- Create your own auth methods

201 response (created) with Location header

```
"response_code": "404" 
"response_msg": "item not found."
"more_info": "https://.../error_codes/#E0000007"
```

Runscope is an api monitor/traffic inspector.

slides posted on speakerdeck

