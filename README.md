github-feature-test
===================

Testing `testing` testing

UTF-8: «W:abc«U:DEF»ghi»

<kbd>C-x 3</kbd>

<kbd>C-x</kbd> <kbd>3</kbd>

<kbd>M-x multicolumn-delete-other-windows-and-split-with-follow-mode RET</kbd>

A test case can be defined as follows:

       (defvar mylang-font-lock-test-dir (faceup-this-file-directory))

       (defun mylang-font-lock-test-apps (file)
         "Test that the mylang FILE is fontifies as the .faceup file describes."
         (faceup-test-font-lock-file 'mylang-mode
                                     (concat mylang-font-lock-test-dir file)))
       (faceup-defexplainer mylang-font-lock-test-apps)

       (ert-deftest mylang-font-lock-file-test ()
         (require 'faceup)
         (should (mylang-font-lock-test-apps "apps/FirstApp/alpha.mylang"))
         (should (mylang-font-lock-test-apps "apps/SecondApp/bravo.mylang")))
