## Create a new widget and display it





使其支持slot

SLATE_SUPPORTS_SLOT( SOverlay::FOverlaySlot )

重载+操作符，使得连续添加slot成为可能



参照 SOverlay 源码





## Widgets Inheritance Tree

**SWidget**

+ SRichTextBlock
+ SMultiLineEditableText

+ **SWeakWidget**

+ **SPanel**
  + **SOverlay**
  + **SBoxPanel**
    + SHorizontalBox
      + SHeader
    + SVerticalBox
  + SBox
    + SEnableBox
    + SSafeZone
  + SWrapBox
  + STooltipPresenter
  + SScrollBarTrack
  + SResponsiveGridPanel
  + SScissorRectBox
  + SRadialBox
  + SCanvas
  + SConstraintCanvas
  + SUniformGridPanel
  + SUniformWrapPanel
  + SWidgetSwitcher
  + SWindowTitleBarArea
  + SWrapBox
  + SDPIScaler
  + SGridPanel
  + SSplitter
  + SMenuAnchor
    + SComboButton
      + SPopupErrorText
+ **SLeafWidget** 叶子部件 其内部不可再添加部件
  + **SImage**
    + **SLayeredImage**
    + SSpinningImage
  + SSpacer
  + STextBlock
  + SProgressBar
+ **SCompoundWidget** 混合部件 与叶子部件相反
  + **SUserWidget**
  + SThrobber
  + SNotificationItem
  + SBreadcrumbTrail
  + SErrorHint
  + SBorder
    + SScrollBar
    + SSeparator
    + SHeaderRow
    + STableRow
    + SErrorText
  + SBackgroundBlur
  + **SWindow**
    + SVirtualWindow
  + SScrollBox
  + SInvalidationPanel
  + SToolTip
  + SScrollBorder
  + SViewport
  + SExpandableArea
  + SExpanderArrow
  + SFxWidget
  + SMenuOwner
  + SPopup
  + SScaleBox
  + STableViewBase
    + SListView
      + STileView
      + STreeView



**SNullWidget**

**SWidegtUtils**





