**Handling new react router dom v6 with class based components:**

Version 6 of react router dom doesn’t supports class based components rather it uses hooks so we will create a react-router-dom utility which works for class based components as well

Create a file named withRouter.js and paste the code: Meaning of the code is explained below:

// this is for using hooks in class based components

import { useLocation, useNavigate, useSearchParams } from "react-router-dom";

export const withRouter = (Component) => {

`  `const Wrapper = (props) => {

// props is components props

`    `const navigate = useNavigate();

`    `let { state } = useLocation();

`    `let [param, setSearchParams] = useSearchParams();

`    `return <Component {...{ state, navigate, param }} {...props} />;

`  `};

`  `return Wrapper;

};

Here we created a withRouter jsx function which takes that **class based components.** The idea is to push the functionality from hooks to Component as a prop. For example if we want to use useNavigate in class based component named Home:

1) Import withRouter
1) Create class based component Home
1) Access navigate as this.props.navigate(‘/’)
1) Module.exports = withRouter(Home);

` `navigate points to useNavigate() in withRouter, so when it is called the actual call goes to withRouter which is not a class based component and it passes the parameter from navigate to useNavigate.
