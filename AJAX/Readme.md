# AJAX :- 	
      Asynchronous JavaScript And XML
			AJAX is a technique for creating fast and dynamic web pages

XMLHttpRequest ke help se karte hai to ye basically 5 steps me divide ho jata hai -- readyState
	0 : request not initialize 						- ham koi bhi request nahi bhejte server ko 
	1 : server connection established 		- isme kya hota ki ham jo apna local system hai or server ka ek connection banate hai uske baad hi ham koi request bhej sakte hai
	2 : request received
	3 : processing request - jo bhi request hamne server ko bheji hai server uspe processing shuru kar deta hai or jese hi server ki processing khata ho jaati hai to last step aata hai
	4 : request fininshed and response is ready 	- request complete ho gayi hai or jo server hai last me hamko response send karte hai 

## ------------------------------------
# var xhttp = new XMLHttpRequest(); // Object banayenge

// readystate ko check karte rehne ke liye
// ye ek tarah ka event ka kaam karta hai matlab ki jese jese hamare readystate ke steps change honge tab automatically ye function apne aap run hota rahega
// iss function ke andar ham ek condition ko check karte hai ki server ka response aya hai ki nahi 
# xhttp.onreadystatechange = function(){
#	if(this.readyState==4 && this.status==2){
#		document.getElementById("demo").innerHTML = this.responseText;
#	}
# }

// jo bhi ham server se file access karna chahate hai ya data access karna chahate hai uske liye do method use karte hai
# xhttp.open("GET", "filename.txt", true);  // param 1-method, 2-filename, 3-async mode
# xhttp.send(); // request server ko send ho jaati hai

// ham yaha pe ek chiz or bhi karte rehte hai ki ham readystate ko check karte rehte hai, jiski help se hame ye pata lag jata hai ki server ka response aya hai ki nahi or jese hi server ka response aa jata hai to ham use HTML me kahi par bhi set kar sakte hai
