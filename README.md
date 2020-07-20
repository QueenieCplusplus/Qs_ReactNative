# Qs_ReactNative

this is my diary to show my improvement in programming, I bought this book in winter in 2018, and can't figure it out for week or weeks, then after 14 months, I retry it again, and get success result, just in 2 hrs. Smile ~

![book](https://github.com/QueenieCplusplus/Qs_ReactNative)



once to be a Native Mobile App Lover and Goer, try a cross-platform hereby now

![react native](https://d1w7fb2mkkr3kw.cloudfront.net/assets/images/book/lrg/9781/4919/9781491989142.jpg)

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
     
![react](https://www.appcoda.com.tw/wp-content/uploads/2015/04/react-native-1024x631.png)
     
# Env 

download npm <https://nodejs.org/en/>

cli see <https://facebook.github.io/react-native/docs/getting-started>

check version 

              $ npm -v
              
              >
              6.13.4
              
install react native app for Node 10+

              $ npm install -g expo-cli
              
              > + expo-cli@3.13.1
              
              $ expo init Project_Name
              
              $ cd under working folder
              
              $ npm start
              
              >>>
              
              React  You can now view Blank Template in the browser.

                Local:            http://localhost:19006/
                On Your Network:  http://192.168.100.24:19006/

              Note that the development build is not optimized.

               › To create a production build, run expo build:web
               › Press Ctrl+C to exit.

               Expo  Press ? to show a list of all available commands.
               
               $ ?
               
> Expo Press
               
                 › Press a to run on Android device/emulator, or i to run on iOS simulator, or w to run on web.
                 › Press c to show info on connecting new devices.
                 › Press d to open DevTools in the default web browser.
                 › Press shift-d to disable automatically opening DevTools at startup.
                 › Press e to send an app link with email.
                 › Press p to toggle production mode. (current mode: development)
                 › Press r to restart bundler, or shift-r to restart and clear cache.
                 › Press s to sign in.

             
alert to upgrade dependencies

              > upgrade your dependencies to the actual version of core-js@3.
              
              $ npm install core-js@3 -u
              
(to be continued...)

search dependency

              $ npm fund
              
              >
                /Users/pintred
                └─┬ core-js@3.6.4
                  ├── type: opencollective
                  └── url: https://opencollective.com/core-js
                  
# npm help

        npm <command> -h  quick help on <command>
        npm -l            display full usage info
        npm help <term>   search for help on <term>
        npm help npm      involved overview
        

# Project Structure


      Root Folder ---|
                     ---- app.json (as manifest)
                     |
                     ---- App.js (source file)
                     |
                     ---- package.json (modules & dependencies)
                     
# App.js

    import React from 'react';
    import { StyleSheet, Text, View } from 'react-native';

    export default function App() {
      return (
        <View style={styles.container}>
          <Text>Open up App.js to start working on your app!</Text>
        </View>
      );
    }

    const styles = StyleSheet.create({
      container: {
        flex: 1,
        backgroundColor: '#fff',
        alignItems: 'center',
        justifyContent: 'center',
      },
    });
    
# Webpack

      Sorry for not giving more info up front :slight_smile:

      For step 1 you just need to find a place to put it. e.g. in your home directory. Do it somewhere that does not already have a subdirectory called expo-cli and the git clone will create the expo-cli directory and put the source code within that.

      Step 2, as you say, is straightforward. It takes a few minutes and spits out a bunch of output. During this “bootstrap” process it builds expo-cli based on the currently checked out version of the expo-cli source code.

      Step 3 is only really needed if you want to make changes to the expo-cli source code and submit it back to the Expo developers for inclusion into the next version of expo-cli. Also yarn start is only useful if you’re going to be making changes to the expo-cli source code.

      After the “bootstrap” process you should find an expo command in the node_modules/.bin/ directory. If you just run expo customize:web it will run your globally installed version of the expo command, because that will be in your PATH, while this newly compiled version will not. There are two ways to run the newly compiled version.

      Specify the full path when you run it, like: /Users/michael/expo-cli/node_modules/.bin/expo customize:web
      Add the node_modules/.bin directory to your PATH before the directory that contains the official version of the expo command. (This can be done permanently or just for the current shell session.)
      You probably want to run the official version of the expo command for everything except the customize:web option, in case there are any bugs in the version compiled from the Git repository. Also, expo customize:web is not something you’re going to have to run every 10 minutes, so I would just go with the first option.

      I have just tried this and was able to get it to generate a webpack.config.js (but I had to first remove the one I had copied there) and also the other files.


