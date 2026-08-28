# React Hook Form

> A performant and flexible library for managing forms and form validation in React applications.

## 🔗 Links

* **Website:** https://react-hook-form.com/
* **Documentation:** https://react-hook-form.com/docs
* **GitHub:** https://github.com/react-hook-form/react-hook-form

## 📌 What is React Hook Form?

React Hook Form is a library that simplifies form management and validation in React applications.

It uses React Hooks and aims to minimize unnecessary re-renders, making it suitable for both simple and complex forms.

## ✨ Key Features

* Form state management
* Input validation
* Minimal re-renders
* Easy integration with UI libraries
* TypeScript support
* Custom validation
* Nested fields
* Dynamic fields
* Error handling

## 🧠 Key Concepts

### `useForm`

The main hook used to manage a form.

```jsx id="q8m3kn"
const {
  register,
  handleSubmit,
  formState: { errors },
} = useForm();
```

### `register`

Connects an input to React Hook Form.

```jsx id="j5r7px"
<input {...register("email")} />
```

### `handleSubmit`

Handles form submission after validation.

```jsx id="c4w9zs"
<form onSubmit={handleSubmit(onSubmit)}>
```

### `formState`

Provides information about the current form state, including validation errors.

## ⚙️ Installation

```bash id="x6p2vq"
npm install react-hook-form
```

## 🧪 Basic Example

```jsx id="n3k8rm"
import { useForm } from "react-hook-form";

function LoginForm() {
  const {
    register,
    handleSubmit,
    formState: { errors },
  } = useForm();

  const onSubmit = (data) => {
    console.log(data);
  };

  return (
    <form onSubmit={handleSubmit(onSubmit)}>
      <input
        {...register("email", {
          required: "Email is required",
        })}
      />

      {errors.email && <p>{errors.email.message}</p>}

      <button type="submit">Submit</button>
    </form>
  );
}
```

## 🔗 Validation

React Hook Form supports validation rules directly through `register`.

```jsx id="v2m6qt"
<input
  {...register("username", {
    required: true,
    minLength: 3,
  })}
/>
```

It can also be integrated with schema validation libraries such as:

* Zod
* Yup
* Joi

## 🎯 Best Used For

* Login forms
* Registration forms
* Checkout forms
* Multi-step forms
* Complex forms
* Forms requiring validation
* React applications with many inputs

## ⚠️ Keep in Mind

React Hook Form is specifically focused on **form state and validation**.

For complex validation logic, pairing it with a schema validation library such as Zod can provide a cleaner and more structured approach.

## 📚 Useful Resources

* Documentation: https://react-hook-form.com/docs
* Get Started: https://react-hook-form.com/get-started
* GitHub: https://github.com/react-hook-form/react-hook-form
