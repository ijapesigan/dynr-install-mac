# Installing the **dynr** R Package on macOS

## 1. Install R
- Download R for macOS ARM from:  
  <https://cloud.r-project.org/bin/macosx/big-sur-arm64/base/R-4.5.1-arm64.pkg>  
- Download R for macOS Intel from:  
  <https://cloud.r-project.org/bin/macosx/big-sur-x86_64/base/R-4.5.1-x86_64.pkg> 
- Double-click the `.pkg` installer and follow the prompts.

## 2. Install Xcode Command Line Tools
- Open Terminal and run:
  ```bash
  xcode-select --install

## 3. Install Homebrew
- Open Terminal and run:
  ```bash
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

## 4. Install GSL
- Open Terminal and run:
  ```bash
  brew install gsl

## 5. Install the dynr Package
- In R, run:  
  ```r
  install.packages("dynr")
- Test the installation with:
  ```r
  source("https://raw.githubusercontent.com/ijapesigan/dynr-install-windows/refs/heads/main/dynr-demo.R")
- A sucessful installation will output the following:
  ```r
  Coefficients:
           Estimate Std. Error t value ci.lower ci.upper Pr(>|t|)    
  spring   -0.10000    0.01583  -6.318 -0.13102 -0.06898   <2e-16 ***
  friction -0.20000    0.03598  -5.558 -0.27053 -0.12947   <2e-16 ***
  dnoise    1.00000    0.15505   6.450  0.69611  1.30389   <2e-16 ***
  mnoise    1.50000    0.08875  16.901  1.32605  1.67395   <2e-16 ***
  inipos    0.00000    1.37080   0.000 -2.68671  2.68671      0.5    
  ---
  Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

  -2 log-likelihood value at convergence = 4214.13
  AIC = 4224.13
  BIC = 4248.67
