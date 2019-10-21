# Fizz-Buzz-2
Bang
import UIKit

class ViewController: UIViewController
{

    override func viewDidLoad()
    {
        super.viewDidLoad()
        
        // Do any additional setup after loading the view, typically from a nib.
    }
    
    override func didReceiveMemoryWarning()
    {
        super.didReceiveMemoryWarning()
        
        // Dispose of any resources that can be recreated.
    }
    
    @IBOutlet weak var enterNum: UITextField!
    
    @IBOutlet var enterBut: UIButton!
    
    @IBOutlet var newNum: UILabel!
    
    @IBAction func buttonPressed(_ sender: Any)
    {
        let numb = Int(enterNum.text!)
        
        newNum.text = fizzBuzz(num: numb!)
    }
    
    func fizzBuzz(num: Int) -> String
    {
        var result = ""
        
        for ir in 1...num
        {
            if ir % 3 == 0 && ir % 5 == 0 && ir % 7 == 0 {
                result += "FizzBuzzBang, "
            }
            else if ir % 3 == 0 && ir % 5 == 0 {
                result += "FizzBuzz, "
            } else if ir % 3 == 0 && ir % 7 == 0 {
                result += "FizzBang, "
            } else if ir % 5 == 0 && ir % 7 == 0 {
                result += "BangBuzz, "
            }
            else if ir % 3 == 0 {
                result += "Fizz, "
            }
            else if ir % 5 == 0 {
                result += "Buzz, "
            }
            else if ir % 7 == 0 {
                result += "Bang, "
            }
            else {
                result += String(ir) + ", "
            }
        }
        return result
    }
    
}
