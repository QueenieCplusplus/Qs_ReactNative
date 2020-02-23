# Qs_ReactNative
once to be a Native Mobile App Lover and Goer, try a cross-platform hereby now

![react native](https://vincent.fishboneapps.com/images/learning/reactNative/reactnativeday7.png)

# Life Cycle


生命週期於呈現畫面 render 方法聆聽到 mountNode 掛載節點開始。
                          
 
       HTML Markup  < - > ReactDOM.render(callback, mountNode)  < - >  Class extends Component
       

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
 
# Import PKG & Tool

    import { tool_name } from "react-native";
    
# inline style object instead of style sheet 

see <https://github.com/facebook/react-native/tree/master/RNTester>

> define a style object

    const styleQ = {
    
      color: 'purple',
      fontSize: '12px'
    
    }

> implement above object to UI object

     const txt = (
     
        <Text style={styleQ}>
        
        Hi ! after 2018 winter,
        I am back to React Native,
        Wish things make them work~
        
        </Text>
     
     ); 
     
# Env 

download npm <https://nodejs.org/en/>
 
