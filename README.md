# UIStepperController

UIStepperController is a custom class that written to  draw / design an awsome Stepper Controller with easy approche. further more it capable of holding either numeric or floating numbers, and developer can customize the stepper controller with attributes such as size, border color, background color, font color. Class is based on Swift language and require UIKit framework for function the functionalities.

![alt text](https://github.com/NadeeshanEngineering/UIStepperController/blob/master/example_preview_screen_shot.png)

To use UIStepperController in your project, please follow following steps

1. Add (or Drag and drop to Your project in Xcode) UIStepperController.swift files to your project 

2. Add UIStepperControllerDelegate to your ViewController class
       Ex:
       
          // Add UIStepperControllerDelegate to ViewController
	        class ViewController: UIViewController, UIStepperControllerDelegate

3. Declare and initialize an UIStepperController instance (Note: Either you can implement UIStepperController as IBOutlet or Subview of your ViewController)

	Ex: (Option - 01) Implement UIStepperController instance as IBOutlet
      
          class ViewController: UIViewController, UIStepperControllerDelegate {
          
                // Implement UIStepperController instance
                @IBOutlet var stepperController: UIStepperController!
                
          }
          
	Ex: (Option - 02) Implement UIStepperController instance as Subview of your ViewController
  
          class ViewController: UIViewController, UIStepperControllerDelegate {
          
                // Implement UIStepperController instance
                let stepperController: UIStepperController = UIStepperController(frame: CGRect(x: 113, y: 150, width: 150, height: 32))
          
          }

4. Assign UIStepperControllerDelegate to instance

          override func viewDidLoad() {
                super.viewDidLoad()
                
                // Assign instance delegate to UIStepperControllerDelegate
                self.stepperController.delegate = self
          }

5. Add UIStepperControllerDelegate functions into your ViewController calss so you can use stepper controller value that change while function

          func stepperDidAddValues(stepper: UIStepperController) {
          
               print("Stepper value did change (Add) : \(stepper.count)")
               
          }

          func stepperDidSubtractValues(stepper: UIStepperController) {
          
               print("Stepper value did change (Subtract) \(stepper.count)")
               
          }
        

Use following atributes to customize your awesome stepper controller

UIStepperController - "textColor" atribute can use developer to change text (foreground) color of stepper controller

    // func - textColor(color: UIColor)
    // Ex:
            self.stepperController.textColor(color: .red)


UIStepperController - "backgroundColor" atribute can use developer to change background color of stepper controller

    // func - backgroundColor(color: UIColor)
    // Ex:
		    self.stepperController.backgroundColor(color: .darkGray)


UIStepperController - "borderColor" atribute can use developer to change border color of stepper controller

    // func - borderColor(color: UIColor)
    // Ex:
		    self.stepperController.borderColor(color: .red)


UIStepperController - "incrementBy" atribute can use developer to change increment weight of stepper controller

    // func - incrementBy(number: CGFloat)
    // Ex:
		    self.stepperController.incrementBy(number: 20.5)
            

UIStepperController - "isMinus" atribute can use developer to change stepper controller to accept minus numbers

    // var - isMinus: Bool = false
    // Ex:
             self.stepperController.isMinus = true


UIStepperController - "isFloat" atribute can use developer to change stepper controller to accept floating numbers

    // var - isFloat: Bool = false
    // Ex:
             self.stepperController.isFloat = true


UIStepperController - "count" atribute can use developer to set and get stepper controller count

    // var - count: CGFloat
    
    // Ex: (set)
             self.stepperController.count = 100.30
             
    // Ex: (get)
             var tValue = self.stepperController.count


Created by Nadeeshan Jayawardana (NEngineering).