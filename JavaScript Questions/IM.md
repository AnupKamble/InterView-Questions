
Given a linked list denoting a number (each key will have numbers from 0-9),
implement addOne function which takes a list and add 1 to it.
Example - For number 7899, Linked List would be [7, 8, 9, 9]

If you add 1 to 7899, you get 7900 which is [7, 9, 0, 0];




/**
 * Given an array [“123f”, “1dsa12”, “1212ds”, “65fd”, “sadfa”, “asdasd”]
 * Each item can contain 0-9, a-z, A-Z where a-z, A-Z characters are unwanted
 * Sum of all the numbers after removing all the unwanted characters 123+112+1212+65
**/




Link : https://www.xyz.com/employee

[
	{
  	"id": 1,
    "name": "XYZ"
  },
  {
  	"id": 1,
    "name": "XYZ"
  },
  {
  	"id": 1,
    "name": "XYZ"
  }
]

Id   Name
1.   XYZ




     function FetchData () {
     
            
            const [State,SetState ] = useState([]);
            
            const FData =()=> {
            
               let res = await fetch(`https://www.xyz.com/employee`);
               let data = await res.json();
                
               SetState(data);
            }
            
            
            useEffect (()=> {
              FData();
            },[]);
            
            
     return (
     
           <> 
           
                   <div>   
                            <h5> </h5>
                   </div>
                
           </>
     )
     }
