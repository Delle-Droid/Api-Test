Figma Link: https://www.figma.com/file/upTxemqUBjfkU7VHjqiubu/AGROVATE?node-id=0%3A1

Create investment request

api path: investments/create
method: POST

{
"name": "Rice farming",
"imageUrl": "https://imageUrl.com/image.png",
"amount": 100,
"duration" : 10,
"company" : "John Doe Inc",
"interestRate": 20,
"datePosted": "2021-07-06",
"availability": "Available",
"location": "Lagos",
"about": "Profitable Rice farming investment in lagos"
}

Sample Response

{
"responseCode": 200,
"responseDescription": "SUCCESS",
"userFriendlyMessage": "Investment created successfully",
"investmentId": 123445
}


Sample failure
{
"responseCode": 400,
"responseDescription": "Bad request",
"userFriendlyMessage": "An error occured while processing your request. Please check your input and try again"
}




====================================
Investment Feed request payload

api path: investments/
Method: GET

====================================


RESPONSE

{
"responseCode": 200,
"responseCodeDescription": "SUCCESS",
"numberOfRecords": 2,
"investments": [
	{
	"id": 12345,
	"name": "Rice farming",
	"imageUrl": "https://imageUrl.com/rice.png",
	"amount": 200,
	"duration" : 10,
	"company" : "John Doe Inc",
	"interestRate": 20,
	"datePosted": "2021-07-06",
	"availability": "Available",
	"location": "Lagos",
	"about": "Profitable Rice farming investment in lagos"
	},
	{
	"id": 12346,
	"name": "Maize farming",
	"imageUrl": "https://imageUrl.com/maize.png",
	"amount": 200,
	"duration" : 10,
	"company" : "John Doe Inc",
	"interestRate": 20,
	"datePosted": "2021-07-06",
	"availability": "Available",
	"location": "Lagos",
	"about": "Profitable Maize farming investment in lagos"
	}
	]
}




====================================
User Investments request payload

api path: investments/user/{userId}
Method: GET
====================================


RESPONSE

{
"responseCode": 200,
"responseCodeDescription": "SUCCESS",
"numberOfRecords": 2,
"investments": [
	{
	"id": 12345,
	"name": "Rice farming",
	"imageUrl": "https://imageUrl.com/rice.png",
	"amount": 200,
	"duration" : 10,
	"company" : "John Doe Inc",
	"interestRate": 20,
	"datePosted": "2021-07-06",
	"availability": "Available",
	"location": "Lagos",
	"about": "Profitable Rice farming investment in lagos"
	},
	{
	"id": 12346,
	"name": "Maize farming",
	"imageUrl": "https://imageUrl.com/maize.png",
	"amount": 200,
	"duration" : 10,
	"company" : "John Doe Inc",
	"interestRate": 20,
	"datePosted": "2021-07-06",
	"availability": "Available",
	"location": "Lagos",
	"about": "Profitable Maize farming investment in lagos"
	}
	]
}




====================================
Products Feed request payload

api path: products/
Method: GET
====================================

RESPONSE

{
"responseCode": 200,
"responseCodeDescription": "SUCCESS",
"numberOfRecords": 2,
"products": [
	{
	"id": 2,
	"name": "Healthy sweet corn",
	"imageUrl": "https://imageUrl.com/corn.png",
	"price": 200,	
	"dealer" : "John Nick Inc",
	"datePosted": "2021-07-06",
	"location": "Lagos",
	"description": "Sweet corn for sale in lagos"
	},
	{
	"id": 4,
	"name": "He-Goat",
	"imageUrl": "https://imageUrl.com/goat.png",
	"price": 200,	
	"dealer" : "John Nick Inc",
	"datePosted": "2021-07-06",
	"location": "Lagos",
	"description": "Healthy he goat for sale in lagos"
	}
	]
}




====================================
Profile / Account Request

api path: profile/{userId}
Method: GET
====================================

RESPONSE

{
"id": 1234,
"firstName": "Kingsley",
"lastName": "Anokam",
"email": "Kingsleyanokam@gmail.com",
"phoneNumber": "2347063834927",
"bvn": "222222222222",
"nin": "55132242322322",
"netWorth": 5000000.00,
"accountType": "Investor",
"dateCreated": "2021-07-06",
"deleted": "N"
}






====================================
User Transactions request payload

api path: transactions/user/{userId}
Method: GET
====================================


RESPONSE

{
"responseCode": 200,
"responseCodeDescription": "SUCCESS",
"numberOfRecords": 2,
"transactions": [
	{
	"id": 12345,
	"accountId": "000123435",
	"status": "SUCCESS",
	"description" : "Investment interest payment",
	"amount" : 200000.00,
	"time": "2021-07-06'T'20:08:45.000",
	"transactionType": "C"
	},
	{
	"id": 12346,
	"accountId": "000123435",
	"status": "SUCCESS",
	"description" : "Payment for Cocoa Investment",
	"amount" : 2000.00,
	"time": "2021-07-06'T'20:08:45.000",
	"transactionType": "D"
	}
	]
}





====================================
ENROLMENT request payload

api path: account/create
Method: POST
====================================


{
"firstName": "Kingsley",
"lastName": "Anokam",
"email": "kingsleyanokam@gmail.com",
"phoneNumber": "2347063834927",
"bvn": "222222222222",
"nin": "55132242322322",
"accountType": "Farmer",
"dateCreated": "2021-07-06",
"password": "#34354?!"
}


RESPONSE


{
"responseCode": 200,
"responseDescription": "SUCCESS",
"userFriendlyMessage": "User kingsleyanokam@gmail.com created successfully"
}



====================================
Login request payload

api path: account/login
Method: POST
====================================


{
"email": "kingsleyanokam@gmail.com",
"password": "#34354?!"
}


RESPONSE

{
"responseCode": 200,
"responseDescription": "SUCCESS",
"userFriendlyMessage": "Login successful"

}

