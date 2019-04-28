# RxAlert

## Overview

We have made it easy to implement UIAlertController using RxSwift.

## Use it

***Via SSH***: For those who plan on regularly making direct commits, cloning over SSH may provide a better experience (which requires uploading SSH keys to GitHub):

```
$ git clone git remote add origin git@github.com:keisukeYamagishi/TabPageScrollViewController.git
```
***Via https***: For those checking out sources as read-only, HTTPS works best:

```
$ git clone https://github.com/keisukeYamagishi/TabPageScrollViewController.git
```

## Sample code

```
alert(title: "RxAlert",
              message: "RxAlert Message",
              actions: [AlertAction(title: "OK", type: 0, style: .default)],
              vc: self).observeOn(MainScheduler.instance)
            .subscribe(onNext: { index in
                print ("index: \(index)")
                
            }).disposed(by: disposeBag)
```
