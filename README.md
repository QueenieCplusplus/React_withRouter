# React_withRouter
this.props.history &amp; hash route such as hash tag to avoid reload page


# React Route Component


 ★ Routing types
 
 
    Since React works with only components, React Router v4 is component based. React Router gives us components like Route, Link, Switch, Prompt etc. to work with. As we discussed, application has to change the view (UI) based on the URL in the browser, but URL can be of different format. URL can be path based like domain/path/nested-path or hash based like domain/#/path/nested-path.
    When hash based URL changes, browser does not reload the page, but that’s not the concern in path based router as well because React Router uses history API. Browser implements this API internally, for things like when you click on an anchor tag and browser loads different page based on different URL, entry of this changed URL is added to the history. Using History API, we can directly manipulate URL in the browser without reloading the page.
    An important thing to remember is, in case of path based routing, a web server needs to be configured to load only one page (e.g. index.html) for any kind of URL. But that’s not the problem in case of hash based routing because you are only loading one page and hashes are not treated as separate pages (routes) on the server. But the big disadvantage of hash based URLs are their incompatibility with Search Engines. You won’t be able to index your website on search engines because search engines do not treat hash bashed URLs as separate URLs, for them domain/#/path is same as domain/#/other-path. But again, if you are bundling your application in .apk using cordova, then use hash based routing, else application won’t work as expected.
    It’s recommended to use path based router whenever you can, so we will go ahead with it.
    React Router (react-router-dom) provided BrowserRouter and HashRouter components which is starting point of your application. As we are using BrowserRouter (path based), we will import it like below in index.js.
    import { BrowserRouter as Router } from 'react-router-dom';
    We have created an alias above because in future, if we had to implement HashRouter, we have to change it at one place only.
    Next step is to wrap our application inside Router component.


★ Code Base
    
    <Router>
        <div>
            { applicationComponents }
        </div>
    </Router>
    
 # Ref Doc
 
 https://medium.com/jspoint/basics-of-react-router-v4-336d274fd9e0
