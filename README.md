## AutoDWG DWGCompareX
DWGCompareX is an Active Control(COM) that helps you find differences between versions of AutoCAD drawings and display them graphically.

### Key features:
- Display the differences in views, using contrasting colors for added entities, deleted entities and modified entities.
- Synchronously zoom the result drawings.
- Synchronously locate the selected entity when you click the result report list.
- Support DWG and DXF in versions from R9 to 2027.

### DWGViewX Interface:


### Free Trial Download Link


## User Guide
### Getting Started
Quick setup

#### Step 1: Register the DLL Component
Double-click `reg.bat` to automatically register `CompareDWGX.ocx` on your system.

If registration fails:
Open Command Prompt as Administrator via:
Start Menu → Windows System → Right-click "Command Prompt" → Run as Administrator

Manually register the DLL using command:
```cmd
regsvr32 CompareDWGX.ocx
```
#### Step 2: Test with Example Html
Run the provided sample Example Html in IE Mode to verify functionality.

**Sample Code**

Sample Code (in VB) for your reference:
```
Dim objImage
Set objImage= CreateObject("AutoDWGCompare.CompareDWG")

objImage.Compare "version1.dwg","version2.dwg"

``` 
Sample Code (in VC) for your reference:
```
#import "D:\\AutoDWGCompare\\CompareDWGX.ocx" named_guids rename_namespace("AutoDWGCompare")
{
CString str1, str2;
CComPtr<AutoDWGCompare::ICompareDWG> conv;
HRESULT hResult = conv.CoCreateInstance(AutoDWGCompare::CLSID_CompareDWG);
str1 = m_strInputFile1;
str2 = m_strInputFile2;
conv->raw_Compare(str1.AllocSysString(), str2.AllocSysString());
}
```
## License Notice
1. Free trial / non-commercial use: GNU LGPL v2.1
2. Commercial production use, closed-source integration requires purchasing our commercial license.

Contact info@autodwg.com for commercial authorization.
