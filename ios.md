 // Create a custom button and set title label style
        
        let orangeButton = UIButton(type: .custom)
        orangeButton.setTitle("Orange", for: UIControlState())
        orangeButton.setTitleColor(.orange, for: UIControlState())
        orangeButton.setTitleColor(.white, for: .highlighted)
        orangeButton.titleLabel?.font = UIFont.systemFont(ofSize: 14)
        orangeButton.contentEdgeInsets = UIEdgeInsetsMake(8, 8, 8, 8)
