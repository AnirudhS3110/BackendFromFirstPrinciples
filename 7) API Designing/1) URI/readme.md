## Parts of URI:
<img src="https://www.winsocketdotnetworkprogramming.com/URIswinsocksocketnetworkprogram5_files/urisocketwinsocknetwork002.png"/> <br>
![alt text](image.png) <br>
1) Schema: Either https or http
2) Authority: Its the Domain OR SubDomain
3) Path: Its basically the path to the Resource you are trying to access
4) Query params: Usually used in GET APIs
5) Fragments: these Navigates us to certain part of the webpage, its like id's of the Div of the part of the page.

## Better Practice:
- Its always better to Deploy the backend in subdomain named ```api```.
- example: ```https://api.example.com```
- Then mention the Version of the API, example:  ```https://api.example.com/v1```
- The NAME of the resource trying to access should always be in Plural Form, example: ```https://api.example.com/v1/books```, even if we want to fetch a SINGLE book, it should always be in Plural Form.
- Never use Underscores of Spaces in Designing route of the API