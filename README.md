# React Form Components

Simple HTML form elements for React.

## Installation

Use the package manager [npm](https://nodejs.org/en/download/) to install @pascalallen/react-form-components.

```bash
npm i @pascalallen/react-form-components
```

## Usage

```typescript jsx
import { ChangeEvent, useState } from "react";
import Form from "./Form";
import InputControl from "./InputControl";

const [emailAddress, setEmailAddress] = useState("");

const handleChange = (event: ChangeEvent<HTMLInputElement>): void => {
  setEmailAddress(event.target.value);
};

<Form>
  <InputControl
    inputId="email"
    className="email"
    name="email"
    type="email"
    label="Email address"
    tabIndex={1}
    value={emailAddress}
    isValid={emailAddress.length > 0}
    required
    error={emailAddress.length < 1 && "Email address is required"}
    onChange={handleChange}
  />
</Form>;
```
