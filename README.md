# Qs_ReactNative
once to be a Native Mobile App Lover and Goer, try a cross-platform hereby now

# Life Cycle

 
       HTML Markup  < - >  ReactDOM.render(call class)  < - >  Class extends React.Component
       

# Bridge Engine in JSX


       class Class_Name extends React.Component {
       
          render(){ //kind of nested func hereby
          
            return React.createElement(this.props.name);
          
          }
       
       }
       
       ReactDOM.render(
       
          React.createElement(Class_Name, { name: "QueenJSX"}),
          mountNode
        
       );
