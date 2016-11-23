Usage
This c# class can be used in application targeting windows store, Xamarin and .Net 4.5 and above frameworks. This Code can be used for implementing Http Operation (Web service Calls) in your application. The class is written in such a way that the developer can customize based on the requirements.


Implementation and Integration
Copy the C# file to your application. The class can do the following operations.
1)	Get Operation
2)	POST Operation 
3)	POST a Form Content
4)	PUT C:\Users\jashif.aboobacke\Documents\Visual Studio 2015\Projects\NetworkHandler\NetworkHandler\README.md
5)	DELETE
6)	GET Binary
The Sample Code is given below.
The RequestBase Class takes 3 parameters. 
1)	URL : the url to be called
2)	HEADERS : If Headers needed for operation. Should be passed in form of IDictionary<string,string>
3)	TIMEOUT: if you want to customize timeout value.
In this parameters 2 and 3 are optional.
String YOUR_URL=http://api.com

Sample Get Operation
RequestBase req = new RequestBase (YOUR_URL, HEADERIFANY, TIMEOUT);        
Var response = await req.GetAsync ();
If (response.IsSuccess && response.Content! = "")
            {
// Do Process the response from response.Content.
            }

Sample Post Operation
For posting a data you can use the post async method which accepts post data and content type parameter.
RequestBase req = new RequestBase (YOUR_URL, HEADERIFANY, TIMEOUT);
Var postdata =Json data /Xml Data.
Content type depends on the data. (“Application/Json” for Json and application/xml for Xml)
Var response = await req.PostAsync (postdata, content type);
If (response.IsSuccess && response.Content! = "")
{
// Do Process the response from response.Content.
}
