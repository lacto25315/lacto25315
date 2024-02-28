$ pip install PyQt5
$ pip show PyQt5
Name: PyQt5
Version: 5.10.1
Summary: Python bindings for the Qt cross platform UI and application toolkit
(略)
Requires: sip
Required-by: 
$ pip show sip
Name: sip
Version: 4.19.8
Summary: Python extension module generator for C and C++ libraries
(略)
Requires: 
Required-by: PyQt5
#!/usr/bin/env python
# coding: utf-8
#

import sys
from PyQt5.QtWidgets import QApplication, QWidget

if __name__ == '__main__':

    app = QApplication(sys.argv)
    widget = QWidget()
    widget.resize(250, 150)
    widget.move(300, 300)
    widget.setWindowTitle('sample')
    widget.show()

    sys.exit(app.exec_())
#!/usr/bin/env python
# coding: utf-8
#

import sys
from PyQt5.QtWidgets import QApplication, QWidget

class ExampleWidget(QWidget):

    def __init__(self):
        super().__init__()
        self.initUI()

    def initUI(self):
        self.resize(250, 150)
        self.move(300, 300)
        self.setWindowTitle('sample')
        self.show()

if __name__ == '__main__':

    app = QApplication(sys.argv)
    ew = ExampleWidget()    
    sys.exit(app.exec_())

