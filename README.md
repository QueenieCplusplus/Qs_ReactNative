# Qs_ReactNative
once to be a Native Mobile App Lover and Goer, try a cross-platform hereby now

![react native](https://vincent.fishboneapps.com/images/learning/reactNative/reactnativeday7.png)

# Life Cycle

 
       HTML Markup  < - > ReactDOM.render(callback)  < - >  Class extends Component
       

# Bridge Engine in JSX

> HTML render React >

       class Class_Name extends React.Component {
       
          render(){ //kind of nested func hereby
          
            return React.createElement(this.props.name);
          
          }
       
       }
       
       ReactDOM.render(
       
          React.createElement(Class_Name, { name: "QueenJSX"}),
          mountNode
        
       );

> using JS-XML -> JSX, to avoid verbos called '.createElement()' >

       class MsgOnHTML extends Component {
       
         render(){
         
           return //html markup 
           // including the {this.props.thing}
         
         }
       
       }
       
       ReactDOM.render(
       
            <MsgOnHTML thing="QsReactNative"/>,
            mountNode
       
       );
       
# Elements in View compars with Native

<div> == <View>
 
<span> == <Text>
 
<li> == <List>
 
<ul> == child items
 
<img> == <Image>
 
 
