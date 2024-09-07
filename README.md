# Xylophone-iOS
<img width="336" alt="Screenshot 2024-09-07 at 9 57 26 PM" src="https://github.com/user-attachments/assets/c35b9a0a-0b55-4a55-8c6f-02dc9e27c527">


A colourful XyloPhone app. Musical Instrument! Music apps are so popular on the App Store that they even get their own category

# Goal

The goal of this is to dive into a simple iOS recipe - how to play sound and use an Apple library called AVFoundation.By learning to use these tools, we’ll be able to start adding custom features to an app and get it to do what you want it to.

# What we will create

We will be making our musical instrument! Music apps are so popular on the App Store that they even get their own category. So in this, we’re going to make a colourful XyloPhone app.

# What we will be using

How to play sound using AVFoundation and AVAudioPlayer.
# Replacement Code

import UIKit
import AVFoundation

class ViewController: UIViewController {
    
    var player: AVAudioPlayer!

    override func viewDidLoad() {
        super.viewDidLoad()
    }

    @IBAction func keyPressed(_ sender: UIButton) {
        playSound()
    }
    
    func playSound() {
        let url = Bundle.main.url(forResource: "C", withExtension: "wav")
        player = try! AVAudioPlayer(contentsOf: url!)
        player.play()
                
    }
}
