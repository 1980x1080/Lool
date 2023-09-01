# NeverLose UI Lib
![NL](![image](https://github.com/1980x1080/Lool/assets/86509034/3c88de4b-a542-4a6f-9f4c-9a79f8905159))

# Script:
```
local library = loadstring(game:HttpGet('https://raw.githubusercontent.com/1980x1080/ApSc/main/seere.vip'))()

local TestTab = library:addTab("Test")
local TestxdTab = TestTab:createGroup('left', 'Test Group')

TestxdTab:addToggle({text = "Toggle Test",default = false,flag = "testedtoggle",callback = function(Value)
	print(Value)
end})

TestxdTab:addSlider({text = "Slider Test", min = 1, max = 100, suffix = "%", float = 1, default = 2, flag = "testedslider",callback = function(Value)
	print(Value)
end})

TestxdTab:addToggle({text = "Toggle+Bind Test",default = false,flag = "testedtogglebind",callback = function(Value)
	print(Value)
end}):addKeybind({text = "Bind Test",type = "toggle",key = Enum.UserInputType.MouseButton2,flag = "testedtogglebindbind"})

TestxdTab:addToggle({text = "Toggle+ColorPicker",default = false,flag = "testedtoggcolorpicler",callback = function(Value)
	print(Value)
end}):addColorpicker({text = "ColorPicker",ontop = true,flag = "testedtoggcolorpiclercolor",color = Color3.fromRGB(255, 255, 255), callback = function(Value)
	print(Value)
end})

TestxdTab:addList({text = "DropDownd Test:",multiselect = false, values = {'1', '2', '3', '4'},flag = "DropDownTested",callback = function(Value)
	print(Value)
end})

TestxdTab:addColorpicker({text = "ColorPicker",ontop = true,flag = "testedcolorpiclercolor",color = Color3.fromRGB(233, 0, 140), callback = function(Value)

end})


local settingsTab = library:addTab("Settings")
local createconfigs = settingsTab:createGroup('left', 'Configs')
createconfigs:addTextbox({text = "CFG Name:",flag = "config_name"})
createconfigs:addButton({text = "Create",callback = library.createConfig})
createconfigs:addConfigbox({flag = 'config_box',values = {}})
createconfigs:addButton({text = "Load",callback = library.loadConfig})
createconfigs:addButton({text = "Update",callback = library.saveConfig})
createconfigs:addButton({text = "Delete",callback = library.deleteConfig})
createconfigs:addButton({text = "Refresh List",callback = library.refreshConfigs})
```
