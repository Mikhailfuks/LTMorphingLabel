import UIKit
import LTMorphingLabel

class ViewController: UIViewController {

  @IBOutlet weak var morphingLabel: LTMorphingLabel!

  override func viewDidLoad() {
    super.viewDidLoad()

    // Set initial text and morphing style
    morphingLabel.text = "Hello, World!"
    morphingLabel.morphingEffect = .evaporate
    
    // Set font and color
    morphingLabel.font = UIFont.systemFont(ofSize: 24)
    morphingLabel.textColor = .blue

    // Start the morphing animation (optional)
    morphingLabel.startAnimating()
  }

  @IBAction func changeText(_ sender: Any) {
    // Change the text and morphing style
    morphingLabel.text = "Morphing Label"
    morphingLabel.morphingEffect = .fall
    
    // Restart the animation
    morphingLabel.startAnimating()
  }
}
