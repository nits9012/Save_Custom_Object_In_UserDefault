# Save_Custom_Object_In_UserDefault


```
class User:NSObject, NSCoding{
    var name:String?
    var address:String?
    var city:String?
    var state:String?
    var country:String?
    
    init(name:String,address:String,city:String,state:String,country:String){
        self.name = name
        self.address = address
        self.city = city
        self.state = state
        self.country = country
    }
    
    required init(coder aDecoder:NSCoder){
        self.name = aDecoder.decodeObject(forKey: "name") as? String
        self.address = aDecoder.decodeObject(forKey: "address") as? String
        self.city = aDecoder.decodeObject(forKey: "city") as? String
        self.state = aDecoder.decodeObject(forKey: "state") as? String
        self.country = aDecoder.decodeObject(forKey: "country") as? String
    }
    
    func encode(with coder: NSCoder) {
        coder.encode(name,forKey: "name")
        coder.encode(address,forKey: "address")
        coder.encode(city,forKey: "city")
        coder.encode(state,forKey: "state")
        coder.encode(state,forKey: "country")
    }
}

```
