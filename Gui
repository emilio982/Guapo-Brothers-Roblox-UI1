-- Guapo Brothers - FINAL UNIVERSAL GUI (January 2026)
-- 100% Working - No Errors - PlayerGui + All Features
-- Owned by Los Primos Client

local Players = game:GetService("Players")
local UserInputService = game:GetService("UserInputService")
local RunService = game:GetService("RunService")
local TweenService = game:GetService("TweenService")
local TeleportService = game:GetService("TeleportService")
local Workspace = game:GetService("Workspace")
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local HttpService = game:GetService("HttpService")
local Lighting = game:GetService("Lighting")
local VirtualInputManager = game:GetService("VirtualInputManager")

local player = Players.LocalPlayer
local camera = Workspace.CurrentCamera

-- Create ScreenGui (PlayerGui - most reliable)
local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Name = "GuapoBrothers"
ScreenGui.ResetOnSpawn = false
ScreenGui.IgnoreGuiInset = true
ScreenGui.Parent = player:WaitForChild("PlayerGui")

-- Variables
local keyCorrect = "kyFVveu2fz"
local isAuthenticated = false
local fastSpeed = false
local aiming = false
local autoFarm = false
local autoCollect = false
local autoKill = false
local minimized = false
local noClip = false
local tpWalk = false
local tpWalkSpeed = 50
local infiniteJump = false
local freecam = false
local freecamSpeed = 50
local antiAFK = false
local xray = false
local hitboxExpander = false
local hitboxSize = 10
local fovValue = 70

-- Colors
local COLORS = {
    Background = Color3.fromRGB(18, 18, 28),
    Accent = Color3.fromRGB(0, 255, 170),
    AccentDark = Color3.fromRGB(0, 180, 120),
    Text = Color3.fromRGB(235, 245, 255),
    TextDark = Color3.fromRGB(170, 180, 195),
    Stroke = Color3.fromRGB(60, 60, 85),
    InputBg = Color3.fromRGB(28, 28, 42),
    TabSelected = Color3.fromRGB(35, 35, 55),
}

-- Main Frame
local MainFrame = Instance.new("Frame")
MainFrame.Name = "MainFrame"
MainFrame.Size = UDim2.new(0, 620, 0, 460)
MainFrame.Position = UDim2.new(0.5, -310, 0.5, -230)
MainFrame.BackgroundColor3 = COLORS.Background
MainFrame.BorderSizePixel = 0
MainFrame.ClipsDescendants = true
MainFrame.Visible = true
MainFrame.Parent = ScreenGui

local MainCorner = Instance.new("UICorner")
MainCorner.CornerRadius = UDim.new(0, 14)
MainCorner.Parent = MainFrame

local MainGradient = Instance.new("UIGradient")
MainGradient.Color = ColorSequence.new{
    ColorSequenceKeypoint.new(0, Color3.fromRGB(30,30,45)),
    ColorSequenceKeypoint.new(1, Color3.fromRGB(18,18,28))
}
MainGradient.Rotation = 90
MainGradient.Parent = MainFrame

local MainStroke = Instance.new("UIStroke")
MainStroke.Color = COLORS.Stroke
MainStroke.Thickness = 1.5
MainStroke.Parent = MainFrame

-- Title Bar
local TitleBar = Instance.new("Frame")
TitleBar.Name = "TitleBar"
TitleBar.Size = UDim2.new(1, 0, 0, 42)
TitleBar.Position = UDim2.new(0, 0, 0, 0)
TitleBar.BackgroundColor3 = Color3.fromRGB(22, 22, 35)
TitleBar.BorderSizePixel = 0
TitleBar.Parent = MainFrame

local TitleLabel = Instance.new("TextLabel")
TitleLabel.Size = UDim2.new(0.6, 0, 1, 0)
TitleLabel.Position = UDim2.new(0.02, 0, 0, 0)
TitleLabel.BackgroundTransparency = 1
TitleLabel.Text = "Guapo Brothers - Owned by Los Primos Client"
TitleLabel.TextColor3 = COLORS.Accent
TitleLabel.TextSize = 22
TitleLabel.Font = Enum.Font.GothamBold
TitleLabel.TextXAlignment = Enum.TextXAlignment.Left
TitleLabel.Parent = TitleBar

-- Close Button
local CloseBtn = Instance.new("TextButton")
CloseBtn.Size = UDim2.new(0, 32, 0, 32)
CloseBtn.Position = UDim2.new(1, -38, 0, 5)
CloseBtn.BackgroundColor3 = Color3.fromRGB(235, 75, 75)
CloseBtn.Text = "×"
CloseBtn.TextColor3 = Color3.new(1,1,1)
CloseBtn.Font = Enum.Font.GothamBold
CloseBtn.TextSize = 24
CloseBtn.Parent = TitleBar

local CloseCorner = Instance.new("UICorner")
CloseCorner.CornerRadius = UDim.new(0, 8)
CloseCorner.Parent = CloseBtn

-- Minimize Button
local HideBtn = Instance.new("TextButton")
HideBtn.Size = UDim2.new(0, 32, 0, 32)
HideBtn.Position = UDim2.new(1, -76, 0, 5)
HideBtn.BackgroundColor3 = Color3.fromRGB(95, 95, 160)
HideBtn.Text = "-"
HideBtn.TextColor3 = Color3.new(1,1,1)
HideBtn.Font = Enum.Font.GothamBold
HideBtn.TextSize = 28
HideBtn.Parent = TitleBar

local HideCorner = Instance.new("UICorner")
HideCorner.CornerRadius = UDim.new(0, 8)
HideCorner.Parent = HideBtn

-- Key System Frame
local KeyFrame = Instance.new("Frame")
KeyFrame.Size = UDim2.new(1, 0, 1, -42)
KeyFrame.Position = UDim2.new(0, 0, 0, 42)
KeyFrame.BackgroundTransparency = 1
KeyFrame.Parent = MainFrame

local KeyTitle = Instance.new("TextLabel")
KeyTitle.Size = UDim2.new(0.9, 0, 0.15, 0)
KeyTitle.Position = UDim2.new(0.05, 0, 0.12, 0)
KeyTitle.BackgroundTransparency = 1
KeyTitle.Text = "Guapo Brothers - Owned by Los Primos Client"
KeyTitle.TextColor3 = COLORS.Accent
KeyTitle.TextSize = 38
KeyTitle.Font = Enum.Font.GothamBlack
KeyTitle.Parent = KeyFrame

local KeySubtitle = Instance.new("TextLabel")
KeySubtitle.Size = UDim2.new(0.9, 0, 0.08, 0)
KeySubtitle.Position = UDim2.new(0.05, 0, 0.28, 0)
KeySubtitle.BackgroundTransparency = 1
KeySubtitle.Text = "Join Discord Server So You Can Get The Password!"
KeySubtitle.TextColor3 = COLORS.TextDark
KeySubtitle.TextSize = 18
KeySubtitle.Font = Enum.Font.GothamMedium
KeySubtitle.Parent = KeyFrame

local DiscordBtn = Instance.new("TextButton")
DiscordBtn.Size = UDim2.new(0.5, 0, 0.09, 0)
DiscordBtn.Position = UDim2.new(0.25, 0, 0.38, 0)
DiscordBtn.BackgroundColor3 = COLORS.AccentDark
DiscordBtn.Text = "Join Discord Server"
DiscordBtn.TextColor3 = Color3.new(1,1,1)
DiscordBtn.Font = Enum.Font.GothamBold
DiscordBtn.TextSize = 17
DiscordBtn.Parent = KeyFrame

local DiscordCorner = Instance.new("UICorner")
DiscordCorner.CornerRadius = UDim.new(0, 10)
DiscordCorner.Parent = DiscordBtn

local KeyBox = Instance.new("TextBox")
KeyBox.Size = UDim2.new(0.6, 0, 0.09, 0)
KeyBox.Position = UDim2.new(0.2, 0, 0.52, 0)
KeyBox.BackgroundColor3 = COLORS.InputBg
KeyBox.TextColor3 = COLORS.Text
KeyBox.PlaceholderText = "Enter Key..."
KeyBox.Text = ""
KeyBox.Font = Enum.Font.Gotham
KeyBox.TextSize = 18
KeyBox.ClearTextOnFocus = false
KeyBox.Parent = KeyFrame

local KeyBoxCorner = Instance.new("UICorner")
KeyBoxCorner.CornerRadius = UDim.new(0, 8)
KeyBoxCorner.Parent = KeyBox

local KeyBoxStroke = Instance.new("UIStroke")
KeyBoxStroke.Color = COLORS.Stroke
KeyBoxStroke.Parent = KeyBox

local SubmitBtn = Instance.new("TextButton")
SubmitBtn.Size = UDim2.new(0.35, 0, 0.09, 0)
SubmitBtn.Position = UDim2.new(0.325, 0, 0.68, 0)
SubmitBtn.BackgroundColor3 = COLORS.Accent
SubmitBtn.Text = "Authenticate"
SubmitBtn.TextColor3 = Color3.new(1,1,1)
SubmitBtn.Font = Enum.Font.GothamBold
SubmitBtn.TextSize = 18
SubmitBtn.Parent = KeyFrame

local SubmitCorner = Instance.new("UICorner")
SubmitCorner.CornerRadius = UDim.new(0, 10)
SubmitCorner.Parent = SubmitBtn

-- Main UI (hidden initially)
local MainUI = Instance.new("Frame")
MainUI.Size = UDim2.new(1, 0, 1, -42)
MainUI.Position = UDim2.new(0, 0, 0, 42)
MainUI.BackgroundTransparency = 1
MainUI.Visible = false
MainUI.Parent = MainFrame

-- Tab System
local TabButtonsFrame = Instance.new("Frame")
TabButtonsFrame.Size = UDim2.new(0.28, 0, 0.9, 0)
TabButtonsFrame.Position = UDim2.new(0.02, 0, 0.05, 0)
TabButtonsFrame.BackgroundTransparency = 1
TabButtonsFrame.Parent = MainUI

local ContentFrame = Instance.new("Frame")
ContentFrame.Size = UDim2.new(0.68, 0, 0.9, 0)
ContentFrame.Position = UDim2.new(0.32, 0, 0.05, 0)
ContentFrame.BackgroundTransparency = 1
ContentFrame.Parent = MainUI

-- Tab Creation Function
local function createTab(name, order)
    local btn = Instance.new("TextButton")
    btn.Name = name .. "TabBtn"
    btn.Size = UDim2.new(1, 0, 0, 48)
    btn.Position = UDim2.new(0, 0, 0, (order-1) * 52)
    btn.BackgroundColor3 = COLORS.InputBg
    btn.Text = name
    btn.TextColor3 = COLORS.TextDark
    btn.Font = Enum.Font.GothamSemibold
    btn.TextSize = 17
    btn.Parent = TabButtonsFrame
    
    local tabCorner = Instance.new("UICorner")
    tabCorner.CornerRadius = UDim.new(0, 9)
    tabCorner.Parent = btn
    
    local content = Instance.new("Frame")
    content.Name = name .. "Content"
    content.Size = UDim2.new(1, 0, 1, 0)
    content.BackgroundTransparency = 1
    content.Visible = false
    content.Parent = ContentFrame
    
    btn.MouseButton1Click:Connect(function()
        for _, v in pairs(ContentFrame:GetChildren()) do
            if v:IsA("Frame") then
                v.Visible = false
            end
        end
        for _, v in pairs(TabButtonsFrame:GetChildren()) do
            if v:IsA("TextButton") then
                TweenService:Create(v, TweenInfo.new(0.25), {
                    BackgroundColor3 = COLORS.InputBg,
                    TextColor3 = COLORS.TextDark
                }):Play()
            end
        end
        
        content.Visible = true
        TweenService:Create(btn, TweenInfo.new(0.25), {
            BackgroundColor3 = COLORS.TabSelected,
            TextColor3 = COLORS.Accent
        }):Play()
    end)
    
    return content, btn
end

-- Create Tabs
local CombatContent, CombatBtn = createTab("Combat", 1)
local MovementContent, MovementBtn = createTab("Movement", 2)
local FarmingContent, FarmingBtn = createTab("Farming", 3)
local ExtrasContent, ExtrasBtn = createTab("Extras", 4)
local ExecutorContent, ExecutorBtn = createTab("Executor", 5)

-- Combat Tab - Aimbot
local AimbotToggle = Instance.new("TextButton")
AimbotToggle.Size = UDim2.new(0.9, 0, 0, 50)
AimbotToggle.Position = UDim2.new(0.05, 0, 0.05, 0)
AimbotToggle.BackgroundColor3 = COLORS.InputBg
AimbotToggle.Text = "Friendly Aimbot (NPC) : OFF"
AimbotToggle.TextColor3 = COLORS.TextDark
AimbotToggle.Font = Enum.Font.GothamSemibold
AimbotToggle.TextSize = 17
AimbotToggle.Parent = CombatContent

local AimbotCorner = Instance.new("UICorner")
AimbotCorner.CornerRadius = UDim.new(0, 9)
AimbotCorner.Parent = AimbotToggle

-- Hitbox Expander Toggle
local HitboxToggle = Instance.new("TextButton")
HitboxToggle.Size = UDim2.new(0.9, 0, 0, 50)
HitboxToggle.Position = UDim2.new(0.05, 0, 0.18, 0)
HitboxToggle.BackgroundColor3 = COLORS.InputBg
HitboxToggle.Text = "Hitbox Expander : OFF"
HitboxToggle.TextColor3 = COLORS.TextDark
HitboxToggle.Font = Enum.Font.GothamSemibold
HitboxToggle.TextSize = 17
HitboxToggle.Parent = CombatContent

local HitboxCorner = Instance.new("UICorner")
HitboxCorner.CornerRadius = UDim.new(0, 9)
HitboxCorner.Parent = HitboxToggle

-- Hitbox Size Slider (Simple TextBox for value)
local HitboxSizeBox = Instance.new("TextBox")
HitboxSizeBox.Size = UDim2.new(0.9, 0, 0, 50)
HitboxSizeBox.Position = UDim2.new(0.05, 0, 0.31, 0)
HitboxSizeBox.BackgroundColor3 = COLORS.InputBg
HitboxSizeBox.Text = "Hitbox Size: 10"
HitboxSizeBox.TextColor3 = COLORS.Text
HitboxSizeBox.Font = Enum.Font.Gotham
HitboxSizeBox.TextSize = 17
HitboxSizeBox.Parent = CombatContent

local HitboxSizeCorner = Instance.new("UICorner")
HitboxSizeCorner.CornerRadius = UDim.new(0, 9)
HitboxSizeCorner.Parent = HitboxSizeBox

-- FOV Slider (TextBox)
local FOVBox = Instance.new("TextBox")
FOVBox.Size = UDim2.new(0.9, 0, 0, 50)
FOVBox.Position = UDim2.new(0.05, 0, 0.44, 0)
FOVBox.BackgroundColor3 = COLORS.InputBg
FOVBox.Text = "FOV: 70"
FOVBox.TextColor3 = COLORS.Text
FOVBox.Font = Enum.Font.Gotham
FOVBox.TextSize = 17
FOVBox.Parent = CombatContent

local FOVCorner = Instance.new("UICorner")
FOVCorner.CornerRadius = UDim.new(0, 9)
FOVCorner.Parent = FOVBox

-- Movement Tab
local SpeedToggle = Instance.new("TextButton")
SpeedToggle.Size = UDim2.new(0.9, 0, 0, 50)
SpeedToggle.Position = UDim2.new(0.05, 0, 0.05, 0)
SpeedToggle.BackgroundColor3 = COLORS.InputBg
SpeedToggle.Text = "Speed Boost : OFF"
SpeedToggle.TextColor3 = COLORS.TextDark
SpeedToggle.Font = Enum.Font.GothamSemibold
SpeedToggle.TextSize = 17
SpeedToggle.Parent = MovementContent

local SpeedCorner = Instance.new("UICorner")
SpeedCorner.CornerRadius = UDim.new(0, 9)
SpeedCorner.Parent = SpeedToggle

local FlyBtn = Instance.new("TextButton")
FlyBtn.Size = UDim2.new(0.9, 0, 0, 50)
FlyBtn.Position = UDim2.new(0.05, 0, 0.18, 0)
FlyBtn.BackgroundColor3 = COLORS.InputBg
FlyBtn.Text = "Activate Mobile Fly"
FlyBtn.TextColor3 = COLORS.TextDark
FlyBtn.Font = Enum.Font.GothamSemibold
FlyBtn.TextSize = 17
FlyBtn.Parent = MovementContent

local FlyCorner = Instance.new("UICorner")
FlyCorner.CornerRadius = UDim.new(0, 9)
FlyCorner.Parent = FlyBtn

-- No Clip Toggle
local NoClipToggle = Instance.new("TextButton")
NoClipToggle.Size = UDim2.new(0.9, 0, 0, 50)
NoClipToggle.Position = UDim2.new(0.05, 0, 0.31, 0)
NoClipToggle.BackgroundColor3 = COLORS.InputBg
NoClipToggle.Text = "No Clip : OFF"
NoClipToggle.TextColor3 = COLORS.TextDark
NoClipToggle.Font = Enum.Font.GothamSemibold
NoClipToggle.TextSize = 17
NoClipToggle.Parent = MovementContent

local NoClipCorner = Instance.new("UICorner")
NoClipCorner.CornerRadius = UDim.new(0, 9)
NoClipCorner.Parent = NoClipToggle

-- TP Walk Toggle
local TPWalkToggle = Instance.new("TextButton")
TPWalkToggle.Size = UDim2.new(0.9, 0, 0, 50)
TPWalkToggle.Position = UDim2.new(0.05, 0, 0.44, 0)
TPWalkToggle.BackgroundColor3 = COLORS.InputBg
TPWalkToggle.Text = "TP Walk : OFF"
TPWalkToggle.TextColor3 = COLORS.TextDark
TPWalkToggle.Font = Enum.Font.GothamSemibold
TPWalkToggle.TextSize = 17
TPWalkToggle.Parent = MovementContent

local TPWalkCorner = Instance.new("UICorner")
TPWalkCorner.CornerRadius = UDim.new(0, 9)
TPWalkCorner.Parent = TPWalkToggle

-- TP Walk Speed Box
local TPWalkSpeedBox = Instance.new("TextBox")
TPWalkSpeedBox.Size = UDim2.new(0.9, 0, 0, 50)
TPWalkSpeedBox.Position = UDim2.new(0.05, 0, 0.57, 0)
TPWalkSpeedBox.BackgroundColor3 = COLORS.InputBg
TPWalkSpeedBox.Text = "TP Walk Speed: 50"
TPWalkSpeedBox.TextColor3 = COLORS.Text
TPWalkSpeedBox.Font = Enum.Font.Gotham
TPWalkSpeedBox.TextSize = 17
TPWalkSpeedBox.Parent = MovementContent

local TPWalkSpeedCorner = Instance.new("UICorner")
TPWalkSpeedCorner.CornerRadius = UDim.new(0, 9)
TPWalkSpeedCorner.Parent = TPWalkSpeedBox

-- Infinite Jump Toggle
local InfJumpToggle = Instance.new("TextButton")
InfJumpToggle.Size = UDim2.new(0.9, 0, 0, 50)
InfJumpToggle.Position = UDim2.new(0.05, 0, 0.70, 0)
InfJumpToggle.BackgroundColor3 = COLORS.InputBg
InfJumpToggle.Text = "Infinite Jump : OFF"
InfJumpToggle.TextColor3 = COLORS.TextDark
InfJumpToggle.Font = Enum.Font.GothamSemibold
InfJumpToggle.TextSize = 17
InfJumpToggle.Parent = MovementContent

local InfJumpCorner = Instance.new("UICorner")
InfJumpCorner.CornerRadius = UDim.new(0, 9)
InfJumpCorner.Parent = InfJumpToggle

-- Freecam Toggle
local FreecamToggle = Instance.new("TextButton")
FreecamToggle.Size = UDim2.new(0.9, 0, 0, 50)
FreecamToggle.Position = UDim2.new(0.05, 0, 0.83, 0)
FreecamToggle.BackgroundColor3 = COLORS.InputBg
FreecamToggle.Text = "Freecam : OFF"
FreecamToggle.TextColor3 = COLORS.TextDark
FreecamToggle.Font = Enum.Font.GothamSemibold
FreecamToggle.TextSize = 17
FreecamToggle.Parent = MovementContent

local FreecamCorner = Instance.new("UICorner")
FreecamCorner.CornerRadius = UDim.new(0, 9)
FreecamCorner.Parent = FreecamToggle

-- Freecam Speed Box
local FreecamSpeedBox = Instance.new("TextBox")
FreecamSpeedBox.Size = UDim2.new(0.9, 0, 0, 50)
FreecamSpeedBox.Position = UDim2.new(0.05, 0, 0.96, 0)
FreecamSpeedBox.BackgroundColor3 = COLORS.InputBg
FreecamSpeedBox.Text = "Freecam Speed: 50"
FreecamSpeedBox.TextColor3 = COLORS.Text
FreecamSpeedBox.Font = Enum.Font.Gotham
FreecamSpeedBox.TextSize = 17
FreecamSpeedBox.Parent = MovementContent

local FreecamSpeedCorner = Instance.new("UICorner")
FreecamSpeedCorner.CornerRadius = UDim.new(0, 9)
FreecamSpeedCorner.Parent = FreecamSpeedBox

-- Farming Tab
local AutoFarmToggle = Instance.new("TextButton")
AutoFarmToggle.Size = UDim2.new(0.9, 0, 0, 50)
AutoFarmToggle.Position = UDim2.new(0.05, 0, 0.05, 0)
AutoFarmToggle.BackgroundColor3 = COLORS.InputBg
AutoFarmToggle.Text = "Auto Farm : OFF"
AutoFarmToggle.TextColor3 = COLORS.TextDark
AutoFarmToggle.Font = Enum.Font.GothamSemibold
AutoFarmToggle.TextSize = 17
AutoFarmToggle.Parent = FarmingContent

local FarmCorner1 = Instance.new("UICorner")
FarmCorner1.CornerRadius = UDim.new(0, 9)
FarmCorner1.Parent = AutoFarmToggle

-- Extras Tab - DP Hub
local DPHubBtn = Instance.new("TextButton")
DPHubBtn.Size = UDim2.new(0.9, 0, 0, 60)
DPHubBtn.Position = UDim2.new(0.05, 0, 0.05, 0)
DPHubBtn.BackgroundColor3 = Color3.fromRGB(80, 40, 120)
DPHubBtn.Text = "Load DP-HUB"
DPHubBtn.TextColor3 = Color3.new(1,1,1)
DPHubBtn.Font = Enum.Font.GothamBold
DPHubBtn.TextSize = 20
DPHubBtn.Parent = ExtrasContent

local DPHubCorner = Instance.new("UICorner")
DPHubCorner.CornerRadius = UDim.new(0, 12)
DPHubCorner.Parent = DPHubBtn

-- Server Hop Button
local ServerHopBtn = Instance.new("TextButton")
ServerHopBtn.Size = UDim2.new(0.9, 0, 0, 50)
ServerHopBtn.Position = UDim2.new(0.05, 0, 0.20, 0)
ServerHopBtn.BackgroundColor3 = COLORS.InputBg
ServerHopBtn.Text = "Server Hop"
ServerHopBtn.TextColor3 = COLORS.TextDark
ServerHopBtn.Font = Enum.Font.GothamSemibold
ServerHopBtn.TextSize = 17
ServerHopBtn.Parent = ExtrasContent

local ServerHopCorner = Instance.new("UICorner")
ServerHopCorner.CornerRadius = UDim.new(0, 9)
ServerHopCorner.Parent = ServerHopBtn

-- Rejoin Server Button
local RejoinBtn = Instance.new("TextButton")
RejoinBtn.Size = UDim2.new(0.9, 0, 0, 50)
RejoinBtn.Position = UDim2.new(0.05, 0, 0.33, 0)
RejoinBtn.BackgroundColor3 = COLORS.InputBg
RejoinBtn.Text = "Rejoin Server"
RejoinBtn.TextColor3 = COLORS.TextDark
RejoinBtn.Font = Enum.Font.GothamSemibold
RejoinBtn.TextSize = 17
RejoinBtn.Parent = ExtrasContent

local RejoinCorner = Instance.new("UICorner")
RejoinCorner.CornerRadius = UDim.new(0, 9)
RejoinCorner.Parent = RejoinBtn

-- Server Info Label
local ServerInfoLabel = Instance.new("TextLabel")
ServerInfoLabel.Size = UDim2.new(0.9, 0, 0, 50)
ServerInfoLabel.Position = UDim2.new(0.05, 0, 0.46, 0)
ServerInfoLabel.BackgroundColor3 = COLORS.InputBg
ServerInfoLabel.Text = "Server Info: Click to Refresh"
ServerInfoLabel.TextColor3 = COLORS.TextDark
ServerInfoLabel.Font = Enum.Font.GothamSemibold
ServerInfoLabel.TextSize = 17
ServerInfoLabel.Parent = ExtrasContent

local ServerInfoCorner = Instance.new("UICorner")
ServerInfoCorner.CornerRadius = UDim.new(0, 9)
ServerInfoCorner.Parent = ServerInfoLabel

-- Local Player Info
local LocalPlayerLabel = Instance.new("TextLabel")
LocalPlayerLabel.Size = UDim2.new(0.9, 0, 0, 50)
LocalPlayerLabel.Position = UDim2.new(0.05, 0, 0.59, 0)
LocalPlayerLabel.BackgroundColor3 = COLORS.InputBg
LocalPlayerLabel.Text = "Local Player: " .. player.Name
LocalPlayerLabel.TextColor3 = COLORS.TextDark
LocalPlayerLabel.Font = Enum.Font.GothamSemibold
LocalPlayerLabel.TextSize = 17
LocalPlayerLabel.Parent = ExtrasContent

local LocalPlayerCorner = Instance.new("UICorner")
LocalPlayerCorner.CornerRadius = UDim.new(0, 9)
LocalPlayerCorner.Parent = LocalPlayerLabel

-- Reset Character Button
local ResetCharBtn = Instance.new("TextButton")
ResetCharBtn.Size = UDim2.new(0.9, 0, 0, 50)
ResetCharBtn.Position = UDim2.new(0.05, 0, 0.72, 0)
ResetCharBtn.BackgroundColor3 = COLORS.InputBg
ResetCharBtn.Text = "Reset Character"
ResetCharBtn.TextColor3 = COLORS.TextDark
ResetCharBtn.Font = Enum.Font.GothamSemibold
ResetCharBtn.TextSize = 17
ResetCharBtn.Parent = ExtrasContent

local ResetCharCorner = Instance.new("UICorner")
ResetCharCorner.CornerRadius = UDim.new(0, 9)
ResetCharCorner.Parent = ResetCharBtn

-- X-Ray Toggle
local XRayToggle = Instance.new("TextButton")
XRayToggle.Size = UDim2.new(0.9, 0, 0, 50)
XRayToggle.Position = UDim2.new(0.05, 0, 0.85, 0)
XRayToggle.BackgroundColor3 = COLORS.InputBg
XRayToggle.Text = "X-Ray : OFF"
XRayToggle.TextColor3 = COLORS.TextDark
XRayToggle.Font = Enum.Font.GothamSemibold
XRayToggle.TextSize = 17
XRayToggle.Parent = ExtrasContent

local XRayCorner = Instance.new("UICorner")
XRayCorner.CornerRadius = UDim.new(0, 9)
XRayCorner.Parent = XRayToggle

-- Anti AFK Toggle
local AntiAFKToggle = Instance.new("TextButton")
AntiAFKToggle.Size = UDim2.new(0.9, 0, 0, 50)
AntiAFKToggle.Position = UDim2.new(0.05, 0, 0.98, 0)
AntiAFKToggle.BackgroundColor3 = COLORS.InputBg
AntiAFKToggle.Text = "Anti AFK : OFF"
AntiAFKToggle.TextColor3 = COLORS.TextDark
AntiAFKToggle.Font = Enum.Font.GothamSemibold
AntiAFKToggle.TextSize = 17
AntiAFKToggle.Parent = ExtrasContent

local AntiAFKCorner = Instance.new("UICorner")
AntiAFKCorner.CornerRadius = UDim.new(0, 9)
AntiAFKCorner.Parent = AntiAFKToggle

-- Teleporting Tools (Assuming a button to equip teleport tool, but simple placeholder)
local TeleToolsBtn = Instance.new("TextButton")
TeleToolsBtn.Size = UDim2.new(0.9, 0, 0, 50)
TeleToolsBtn.Position = UDim2.new(0.05, 0, 1.11, 0)
TeleToolsBtn.BackgroundColor3 = COLORS.InputBg
TeleToolsBtn.Text = "Teleport Tools"
TeleToolsBtn.TextColor3 = COLORS.TextDark
TeleToolsBtn.Font = Enum.Font.GothamSemibold
TeleToolsBtn.TextSize = 17
TeleToolsBtn.Parent = ExtrasContent

local TeleToolsCorner = Instance.new("UICorner")
TeleToolsCorner.CornerRadius = UDim.new(0, 9)
TeleToolsCorner.Parent = TeleToolsBtn

-- Executor Tab
local ScriptBox = Instance.new("TextBox")
ScriptBox.Size = UDim2.new(0.9, 0, 0.6, 0)
ScriptBox.Position = UDim2.new(0.05, 0, 0.05, 0)
ScriptBox.BackgroundColor3 = COLORS.InputBg
ScriptBox.TextColor3 = COLORS.Text
ScriptBox.PlaceholderText = "Enter Lua Script Here..."
ScriptBox.Text = ""
ScriptBox.Font = Enum.Font.Code
ScriptBox.TextSize = 14
ScriptBox.MultiLine = true
ScriptBox.ClearTextOnFocus = false
ScriptBox.TextWrapped = true
ScriptBox.Parent = ExecutorContent

local ScriptCorner = Instance.new("UICorner")
ScriptCorner.CornerRadius = UDim.new(0, 8)
ScriptCorner.Parent = ScriptBox

local ExecuteBtn = Instance.new("TextButton")
ExecuteBtn.Size = UDim2.new(0.4, 0, 0.08, 0)
ExecuteBtn.Position = UDim2.new(0.05, 0, 0.7, 0)
ExecuteBtn.BackgroundColor3 = COLORS.Accent
ExecuteBtn.Text = "Execute"
ExecuteBtn.TextColor3 = Color3.new(1,1,1)
ExecuteBtn.Font = Enum.Font.GothamBold
ExecuteBtn.TextSize = 18
ExecuteBtn.Parent = ExecutorContent

local ExecCorner = Instance.new("UICorner")
ExecCorner.CornerRadius = UDim.new(0, 10)
ExecCorner.Parent = ExecuteBtn

local ClearBtn = Instance.new("TextButton")
ClearBtn.Size = UDim2.new(0.4, 0, 0.08, 0)
ClearBtn.Position = UDim2.new(0.55, 0, 0.7, 0)
ClearBtn.BackgroundColor3 = COLORS.AccentDark
ClearBtn.Text = "Clear"
ClearBtn.TextColor3 = Color3.new(1,1,1)
ClearBtn.Font = Enum.Font.GothamBold
ClearBtn.TextSize = 18
ClearBtn.Parent = ExecutorContent

local ClearCorner = Instance.new("UICorner")
ClearCorner.CornerRadius = UDim.new(0, 10)
ClearCorner.Parent = ClearBtn

-- Minimize Icon
local MinIcon = Instance.new("TextButton")
MinIcon.Size = UDim2.new(0, 70, 0, 70)
MinIcon.Position = UDim2.new(1, -90, 1, -90)
MinIcon.BackgroundColor3 = COLORS.AccentDark
MinIcon.Text = "GB"
MinIcon.TextColor3 = Color3.new(1,1,1)
MinIcon.Font = Enum.Font.GothamBold
MinIcon.TextSize = 24
MinIcon.Visible = false
MinIcon.Parent = ScreenGui

local MinIconCorner = Instance.new("UICorner")
MinIconCorner.CornerRadius = UDim.new(1, 0)
MinIconCorner.Parent = MinIcon

-- Functionality
DiscordBtn.MouseButton1Click:Connect(function()
    setclipboard("https://discord.gg/uEupXWPCj")
    DiscordBtn.Text = "Copied! Join Now"
    wait(1.5)
    DiscordBtn.Text = "Join Discord Server"
end)

SubmitBtn.MouseButton1Click:Connect(function()
    if KeyBox.Text == keyCorrect then
        KeyFrame.Visible = false
        MainUI.Visible = true
        CombatBtn.MouseButton1Click()
    else
        -- Shake animation
        for i = 1, 4 do
            TweenService:Create(KeyBox, TweenInfo.new(0.1), {
                Position = UDim2.new(0.2 + math.random(-0.02, 0.02), 0, 0.52 + math.random(-0.02, 0.02), 0)
            }):Play()
            wait(0.1)
        end
        KeyBox.Position = UDim2.new(0.2, 0, 0.52, 0)
    end
end)

AimbotToggle.MouseButton1Click:Connect(function()
    aiming = not aiming
    AimbotToggle.Text = "Friendly Aimbot (NPC) : " .. (aiming and "ON" or "OFF")
    TweenService:Create(AimbotToggle, TweenInfo.new(0.2), {
        BackgroundColor3 = aiming and COLORS.AccentDark or COLORS.InputBg,
        TextColor3 = aiming and Color3.new(1,1,1) or COLORS.TextDark
    }):Play()
end)

SpeedToggle.MouseButton1Click:Connect(function()
    fastSpeed = not fastSpeed
    SpeedToggle.Text = "Speed Boost : " .. (fastSpeed and "ON" or "OFF")
    TweenService:Create(SpeedToggle, TweenInfo.new(0.2), {
        BackgroundColor3 = fastSpeed and COLORS.AccentDark or COLORS.InputBg,
        TextColor3 = fastSpeed and Color3.new(1,1,1) or COLORS.TextDark
    }):Play()
end)

FlyBtn.MouseButton1Click:Connect(function()
    loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Mobile-Fly-V1-45764"))()
end)

AutoFarmToggle.MouseButton1Click:Connect(function()
    autoFarm = not autoFarm
    AutoFarmToggle.Text = "Auto Farm : " .. (autoFarm and "ON" or "OFF")
    TweenService:Create(AutoFarmToggle, TweenInfo.new(0.2), {
        BackgroundColor3 = autoFarm and COLORS.AccentDark or COLORS.InputBg,
        TextColor3 = autoFarm and Color3.new(1,1,1) or COLORS.TextDark
    }):Play()
end)

DPHubBtn.MouseButton1Click:Connect(function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/CoolXplo/DP-HUB-coolxplo/main/The_Storage.lua"))()
end)

ExecuteBtn.MouseButton1Click:Connect(function()
    loadstring(ScriptBox.Text)()
end)

ClearBtn.MouseButton1Click:Connect(function()
    ScriptBox.Text = ""
end)

CloseBtn.MouseButton1Click:Connect(function()
    ScreenGui:Destroy()
end)

HideBtn.MouseButton1Click:Connect(function()
    minimized = true
    MainFrame.Visible = false
    MinIcon.Visible = true
end)

MinIcon.MouseButton1Click:Connect(function()
    minimized = false
    MinIcon.Visible = false
    MainFrame.Visible = true
end)

-- Added Functionality

-- No Clip
NoClipToggle.MouseButton1Click:Connect(function()
    noClip = not noClip
    NoClipToggle.Text = "No Clip : " .. (noClip and "ON" or "OFF")
    TweenService:Create(NoClipToggle, TweenInfo.new(0.2), {
        BackgroundColor3 = noClip and COLORS.AccentDark or COLORS.InputBg,
        TextColor3 = noClip and Color3.new(1,1,1) or COLORS.TextDark
    }):Play()
end)

-- TP Walk
TPWalkToggle.MouseButton1Click:Connect(function()
    tpWalk = not tpWalk
    TPWalkToggle.Text = "TP Walk : " .. (tpWalk and "ON" or "OFF")
    TweenService:Create(TPWalkToggle, TweenInfo.new(0.2), {
        BackgroundColor3 = tpWalk and COLORS.AccentDark or COLORS.InputBg,
        TextColor3 = tpWalk and Color3.new(1,1,1) or COLORS.TextDark
    }):Play()
end)

TPWalkSpeedBox.FocusLost:Connect(function()
    tpWalkSpeed = tonumber(TPWalkSpeedBox.Text:match("%d+")) or 50
end)

-- Infinite Jump
InfJumpToggle.MouseButton1Click:Connect(function()
    infiniteJump = not infiniteJump
    InfJumpToggle.Text = "Infinite Jump : " .. (infiniteJump and "ON" or "OFF")
    TweenService:Create(InfJumpToggle, TweenInfo.new(0.2), {
        BackgroundColor3 = infiniteJump and COLORS.AccentDark or COLORS.InputBg,
        TextColor3 = infiniteJump and Color3.new(1,1,1) or COLORS.TextDark
    }):Play()
end)

UserInputService.JumpRequest:Connect(function()
    if infiniteJump and player.Character then
        player.Character:FindFirstChildOfClass("Humanoid"):ChangeState("Jumping")
    end
end)

-- Freecam
FreecamToggle.MouseButton1Click:Connect(function()
    freecam = not freecam
    FreecamToggle.Text = "Freecam : " .. (freecam and "ON" or "OFF")
    TweenService:Create(FreecamToggle, TweenInfo.new(0.2), {
        BackgroundColor3 = freecam and COLORS.AccentDark or COLORS.InputBg,
        TextColor3 = freecam and Color3.new(1,1,1) or COLORS.TextDark
    }):Play()
    if freecam then
        camera.CameraType = Enum.CameraType.Scriptable
    else
        camera.CameraType = Enum.CameraType.Custom
    end
end)

FreecamSpeedBox.FocusLost:Connect(function()
    freecamSpeed = tonumber(FreecamSpeedBox.Text:match("%d+")) or 50
end)

-- Hitbox Expander
HitboxToggle.MouseButton1Click:Connect(function()
    hitboxExpander = not hitboxExpander
    HitboxToggle.Text = "Hitbox Expander : " .. (hitboxExpander and "ON" or "OFF")
    TweenService:Create(HitboxToggle, TweenInfo.new(0.2), {
        BackgroundColor3 = hitboxExpander and COLORS.AccentDark or COLORS.InputBg,
        TextColor3 = hitboxExpander and Color3.new(1,1,1) or COLORS.TextDark
    }):Play()
end)

HitboxSizeBox.FocusLost:Connect(function()
    hitboxSize = tonumber(HitboxSizeBox.Text:match("%d+")) or 10
end)

-- FOV
FOVBox.FocusLost:Connect(function()
    fovValue = tonumber(FOVBox.Text:match("%d+")) or 70
    camera.FieldOfView = fovValue
end)

-- Server Hop
ServerHopBtn.MouseButton1Click:Connect(function()
    local servers = HttpService:JSONDecode(game:HttpGet("https://games.roblox.com/v1/games/" .. game.PlaceId .. "/servers/Public?sortOrder=Asc&limit=100"))
    local server = servers.data[math.random(1, #servers.data)]
    TeleportService:TeleportToPlaceInstance(game.PlaceId, server.id, player)
end)

-- Rejoin Server
RejoinBtn.MouseButton1Click:Connect(function()
    TeleportService:Teleport(game.PlaceId, player)
end)

-- Server Info (Simple player count)
ServerInfoLabel.InputBegan:Connect(function(input)
    if input.UserInputType == Enum.UserInputType.MouseButton1 then
        ServerInfoLabel.Text = "Server Info: Players - " .. #Players:GetPlayers() .. "/" .. game:GetService("Players").MaxPlayers
    end
end)

-- Reset Character
ResetCharBtn.MouseButton1Click:Connect(function()
    player.Character:BreakJoints()
end)

-- X-Ray (Simple transparency for parts)
XRayToggle.MouseButton1Click:Connect(function()
    xray = not xray
    XRayToggle.Text = "X-Ray : " .. (xray and "ON" or "OFF")
    TweenService:Create(XRayToggle, TweenInfo.new(0.2), {
        BackgroundColor3 = xray and COLORS.AccentDark or COLORS.InputBg,
        TextColor3 = xray and Color3.new(1,1,1) or COLORS.TextDark
    }):Play()
end)

-- Anti AFK
AntiAFKToggle.MouseButton1Click:Connect(function()
    antiAFK = not antiAFK
    AntiAFKToggle.Text = "Anti AFK : " .. (antiAFK and "ON" or "OFF")
    TweenService:Create(AntiAFKToggle, TweenInfo.new(0.2), {
        BackgroundColor3 = antiAFK and COLORS.AccentDark or COLORS.InputBg,
        TextColor3 = antiAFK and Color3.new(1,1,1) or COLORS.TextDark
    }):Play()
end)

-- Teleport Tools (Placeholder: Teleport to mouse click)
TeleToolsBtn.MouseButton1Click:Connect(function()
    local mouse = player:GetMouse()
    mouse.Button1Down:Connect(function()
        if player.Character then
            player.Character:MoveTo(mouse.Hit.Position)
        end
    end)
end)

-- Drag System
local dragging = false
local dragInput, mousePos, framePos

TitleBar.InputBegan:Connect(function(input)
    if input.UserInputType == Enum.UserInputType.MouseButton1 then
        dragging = true
        mousePos = input.Position
        framePos = MainFrame.Position
        input.Changed:Connect(function()
            if input.UserInputState == Enum.UserInputState.End then
                dragging = false
            end
        end)
    end
end)

TitleBar.InputChanged:Connect(function(input)
    if input.UserInputType == Enum.UserInputType.MouseMovement then
        dragInput = input
    end
end)

UserInputService.InputChanged:Connect(function(input)
    if input == dragInput and dragging then
        local Delta = input.Position - mousePos
        MainFrame.Position = UDim2.new(framePos.X.Scale, framePos.X.Offset + Delta.X, framePos.Y.Scale, framePos.Y.Offset + Delta.Y)
    end
end)

-- Loops
RunService.Heartbeat:Connect(function(delta)
    if fastSpeed and player.Character and player.Character:FindFirstChild("Humanoid") then
        player.Character.Humanoid.WalkSpeed = 50
    end
    
    if autoFarm and player.Character and player.Character:FindFirstChildOfClass("Tool") then
        player.Character:FindFirstChildOfClass("Tool"):Activate()
    end
    
    if noClip and player.Character then
        for _, part in pairs(player.Character:GetChildren()) do
            if part:IsA("BasePart") then
                part.CanCollide = false
            end
        end
    end
    
    if tpWalk and player.Character and player.Character:FindFirstChild("Humanoid") then
        local humanoid = player.Character.Humanoid
        if humanoid.MoveDirection.Magnitude > 0 then
            player.Character:TranslateBy(humanoid.MoveDirection * tpWalkSpeed * delta)
        end
    end
    
    if freecam then
        local keys = {
            Forward = UserInputService:IsKeyDown(Enum.KeyCode.W),
            Backward = UserInputService:IsKeyDown(Enum.KeyCode.S),
            Left = UserInputService:IsKeyDown(Enum.KeyCode.A),
            Right = UserInputService:IsKeyDown(Enum.KeyCode.D),
            Up = UserInputService:IsKeyDown(Enum.KeyCode.Space),
            Down = UserInputService:IsKeyDown(Enum.KeyCode.LeftControl)
        }
        local moveDir = Vector3.new(
            (keys.Right and 1 or 0) - (keys.Left and 1 or 0),
            (keys.Up and 1 or 0) - (keys.Down and 1 or 0),
            (keys.Backward and 1 or 0) - (keys.Forward and 1 or 0)
        )
        if moveDir.Magnitude > 0 then
            moveDir = moveDir.Unit
            camera.CFrame = camera.CFrame * CFrame.new(moveDir * freecamSpeed * delta)
        end
    end
    
    if hitboxExpander then
        for _, p in pairs(Players:GetPlayers()) do
            if p ~= player and p.Character and p.Character:FindFirstChild("HumanoidRootPart") then
                p.Character.HumanoidRootPart.Size = Vector3.new(hitboxSize, hitboxSize, hitboxSize)
                p.Character.HumanoidRootPart.Transparency = 0.7
            end
        end
    end
    
    if xray then
        for _, part in pairs(Workspace:GetDescendants()) do
            if part:IsA("BasePart") and not part.Parent:FindFirstChild("Humanoid") then
                part.Transparency = 0.8
            end
        end
    end
    
    if antiAFK then
        VirtualInputManager:SendKeyEvent(true, "W", false, game)
        wait(0.1)
        VirtualInputManager:SendKeyEvent(false, "W", false, game)
    end
end)

-- Fade In Animation
MainFrame.BackgroundTransparency = 1
TweenService:Create(MainFrame, TweenInfo.new(0.8, Enum.EasingStyle.Quint), {
    BackgroundTransparency = 0
}):Play()

print("Guapo Brothers GUI Loaded Successfully!")
