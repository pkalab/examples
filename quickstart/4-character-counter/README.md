
⏳  **ADDING CHARACTER COUNTER**⏳  \
In the first section, we explored browser-to-browser messaging using local, i.e. browser-native, services and the Fluence network for message transport.

In the second section, we developed a HelloWorld Wasm module and deployed it as a hosted service on the testnet peer 12D3KooWFEwNWcHqi9rtsmDhsYcDbRUCDXH84RC4FW6UfsFWaoHi with service id 1e740ce4-81f6-4dd4-9bed-8d86e9c2fa50 . 

Finally, we extended our browser-to-browser messaging application with our hosted service.
Let's navigate to the 4-character-counter directory in the VSCode terminal and install the dependencies: 

```
npm install
```
And run the application with: 
```
npm start
``` 
\
Which will open a new browser tab at http://localhost:3000 . \
Following the instructions, we connect to any one of the displayed relay ids, open another browser tab also at http://localhost:3000, select a relay and copy and paste the client peer id and relay id into corresponding fields in the first tab and press the say hello button.

 We can see two different counters. One that counts with spaces and one without.\
 ![alt text](https://user-images.githubusercontent.com/57189190/132883177-b29a8451-8828-445e-8840-3e5820b69dc3.jpg) \
Let's take a look on a App.tsx file \
![alt text](https://user-images.githubusercontent.com/57189190/132883182-eacdf511-aaba-46f8-856a-8a97815fbb26.jpg) \
If we scroll down to HTML elements we can see that we appended {helloMessage} variable \
helloMessage.length - counts with spaces \
(helloMessage.length)-(helloMessage.split(" ").length - 1) - counts without spaces. \
To count without spaces we implemented regex function and subtract length from regex variable 
