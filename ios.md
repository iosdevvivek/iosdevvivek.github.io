 // Create a custom button and set title label style
        
        let orangeButton = UIButton(type: .custom)
        orangeButton.setTitle("Orange", for: UIControlState())
        orangeButton.setTitleColor(.orange, for: UIControlState())
        orangeButton.setTitleColor(.white, for: .highlighted)
        orangeButton.titleLabel?.font = UIFont.systemFont(ofSize: 14)
        orangeButton.contentEdgeInsets = UIEdgeInsetsMake(8, 8, 8, 8)
// back ground image..
      orangeButton.setBackgroundImage(slicedBorderTemplate, for: UIControlState())
        orangeButton.setBackgroundImage(slicedFillTemplate, for: .highlighted)
        
        
 // table View in swift..
 
  func numberOfSections(in tableView: UITableView) -> Int {
        return 1
    }

    func tableView(_ tableView: UITableView, numberOfRowsInSection section: Int) -> Int {
        return locations.count
    }

    func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
        let cell = tableView.dequeueReusableCell(withIdentifier: LocationCell.reuseIdentifier, for: indexPath)
        configure(cell: cell, indexPath: indexPath)
        return cell
    }
     private func configure(cell: UITableViewCell, indexPath: IndexPath) {
        if let cell = cell as? LocationCell {
            let object = locations[indexPath.row]
            cell.configure(object: object)
        } }
        
     // extention in UIview
     
     extension UIView {

    
    open var superview: UIView? { get }

    open var subviews: [UIView] { get }

    open var window: UIWindow? { get }

    
    open func removeFromSuperview()

    open func insertSubview(_ view: UIView, at index: Int)

    open func exchangeSubview(at index1: Int, withSubviewAt index2: Int)

    
    open func addSubview(_ view: UIView)

    open func insertSubview(_ view: UIView, belowSubview siblingSubview: UIView)

    open func insertSubview(_ view: UIView, aboveSubview siblingSubview: UIView)

    
    open func bringSubview(toFront view: UIView)

    open func sendSubview(toBack view: UIView)

    
    open func didAddSubview(_ subview: UIView)

    open func willRemoveSubview(_ subview: UIView)

    
    open func willMove(toSuperview newSuperview: UIView?)

    open func didMoveToSuperview()

    open func willMove(toWindow newWindow: UIWindow?)

    open func didMoveToWindow()

    
    open func isDescendant(of view: UIView) -> Bool // returns YES for self.

    open func viewWithTag(_ tag: Int) -> UIView? // recursive search. includes self

    
    // Allows you to perform layout before the drawing cycle happens. -layoutIfNeeded forces layout early
    open func setNeedsLayout()

    open func layoutIfNeeded()

    
    open func layoutSubviews() // override point. called by layoutIfNeeded automatically. As of iOS 6.0, when constraints-based layout is used the base implementation applies the constraints-based layout, otherwise it does nothing.

    
    /*
     -layoutMargins returns a set of insets from the edge of the view's bounds that denote a default spacing for laying out content.
     If preservesSuperviewLayoutMargins is YES, margins cascade down the view tree, adjusting for geometry offsets, so that setting the left value of layoutMargins on a superview will affect the left value of layoutMargins for subviews positioned close to the left edge of their superview's bounds
     If your view subclass uses layoutMargins in its layout or drawing, override -layoutMarginsDidChange in order to refresh your view if the margins change.
     */
    @available(iOS 8.0, *)
    open var layoutMargins: UIEdgeInsets

    @available(iOS 8.0, *)
    open var preservesSuperviewLayoutMargins: Bool // default is NO - set to enable pass-through or cascading behavior of margins from this view’s parent to its children

    @available(iOS 8.0, *)
    open func layoutMarginsDidChange()

    
    /* The edges of this guide are constrained to equal the edges of the view inset by the layoutMargins
     */
    @available(iOS 9.0, *)
    open var layoutMarginsGuide: UILayoutGuide { get }

    
    /// This content guide provides a layout area that you can use to place text and related content whose width should generally be constrained to a size that is easy for the user to read. This guide provides a centered region that you can place content within to get this behavior for this view.
    @available(iOS 9.0, *)
    open var readableContentGuide: UILayoutGuide { get }
}

 
 
        
