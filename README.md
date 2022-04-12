local RayXLauncher = Instance.new("ScreenGui")
local MainFrame = Instance.new("Frame")
local Frame = Instance.new("Frame")
local Frame_2 = Instance.new("Frame")
local TextLabel = Instance.new("TextLabel")
local LAUNCH = Instance.new("TextButton")
local EXIT = Instance.new("TextButton")

--Properties:

RayXLauncher.Name = "RayXLauncher"
RayXLauncher.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
RayXLauncher.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

MainFrame.Name = "MainFrame"
MainFrame.Parent = RayXLauncher
MainFrame.BackgroundColor3 = Color3.fromRGB(0, 0, 21)
MainFrame.Position = UDim2.new(0.122191027, 0, 0.267056525, 0)
MainFrame.Size = UDim2.new(0, 595, 0, 313)
MainFrame.Active = true
MainFrame.Draggable = true

Frame.Parent = MainFrame
Frame.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
Frame.Size = UDim2.new(0, 477, 0, 31)

Frame_2.Parent = Frame
Frame_2.BackgroundColor3 = Color3.fromRGB(255, 0, 4)
Frame_2.Position = UDim2.new(0, 0, 1, 0)
Frame_2.Size = UDim2.new(0, 595, 0, 6)

TextLabel.Parent = Frame
TextLabel.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
TextLabel.Size = UDim2.new(0, 595, 0, 31)
TextLabel.Font = Enum.Font.SourceSans
TextLabel.Text = "RAYX LAUNCHER"
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextSize = 24.000

LAUNCH.Name = "LAUNCH"
LAUNCH.Parent = MainFrame
LAUNCH.BackgroundColor3 = Color3.fromRGB(255, 0, 4)
LAUNCH.Position = UDim2.new(0.316198945, 0, 0.266885668, 0)
LAUNCH.Size = UDim2.new(0, 200, 0, 50)
LAUNCH.Font = Enum.Font.Cartoon
LAUNCH.Text = "Launch RayX"
LAUNCH.TextColor3 = Color3.fromRGB(36, 36, 36)
LAUNCH.TextSize = 14.000

EXIT.Name = "EXIT"
EXIT.Parent = RayXLauncher
EXIT.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
EXIT.Position = UDim2.new(0.313326776, 0, 0.61403507, 0)
EXIT.Size = UDim2.new(0, 200, 0, 50)
EXIT.Font = Enum.Font.SourceSans
EXIT.Text = "EXIT LAUNCHER"
EXIT.TextColor3 = Color3.fromRGB(0, 0, 0)
EXIT.TextSize = 14.000

-- Scripts:

local function HNHTM_fake_script() -- EXIT.LocalScript 
	local script = Instance.new('LocalScript', EXIT)

	local function OnClicked()
		script.Parent.Parent:Remove()
	end
	
	script.Parent.MouseButton1Click:connect(OnClicked)
end
coroutine.wrap(HNHTM_fake_script)()
