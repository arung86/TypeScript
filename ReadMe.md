# TypeScript Examples

## Inheritance 
```TypeScript
class Report{
 data : string[];
 
 constructor(data: string[]){
    this.data = data;
 }
 run(){
  this.data.forEach(function(line){ console.log(line)});
 }
}

//#Example 1
var report: Report = new Report(['First Line', 'Second Line']);
report.run();

class TabbedReport extends Report{
    headers: string[];
    constructor(headers: string[], values: string[]) {         
        super(values);
        this.headers = headers;
    }
    run() {
        console.log(this.headers[0]);
        super.run();
    }
}
```

## Arrow Functions
```typscript
//#Example 2

var headers: string[] = ['Name'];
var data: string[] = ['Alice Green', 'Paul Pfifer', 'Louis Blakenship'];
var tabReport: TabbedReport = new TabbedReport(headers, data);
tabReport.run();


//# Example 3 - Arrow Functions 

var evens = [0, 2, 4, 6, 8];
var odds = evens.map(even => even + 1);
console.log(odds);
data.forEach(line => console.log(line));


//# Example 4 

var nate = {
    name: "Nate",
    guitars: ["Gibson", "Martin", "Taylor"],
    printGuitars() {
        self = this;
        this.guitars.forEach(function (g) {
            console.log(self.name + ' plays a ' + g)
        });
    }
};

nate.printGuitars();
```
//###########################################################
