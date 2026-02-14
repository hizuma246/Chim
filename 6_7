local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()
local PlaceID = game.PlaceId

-- [[ 1. CẤU HÌNH NÚT BẤM TRÒN ]] --
local ScreenGui = Instance.new("ScreenGui")
local ImageButton = Instance.new("ImageButton")
local UICorner = Instance.new("UICorner")

ScreenGui.Parent = game.CoreGui
ImageButton.Parent = ScreenGui
ImageButton.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
ImageButton.Size = UDim2.new(0, 45, 0, 45)
ImageButton.Position = UDim2.new(0.1, 0, 0.15, 0)
ImageButton.Draggable = true
ImageButton.Active = true
ImageButton.Image = "http://www.roblox.com/asset/?id=83190276951914"
UICorner.CornerRadius = UDim.new(1, 0)
UICorner.Parent = ImageButton

-- [[ 2. KHỞI TẠO WINDOW ]] --
local Window = Fluent:CreateWindow({
    Title = "TBoy Roblox Tổng Hợp",
    SubTitle = "Hệ Thống Tự Nhận Diện Game",
    TabWidth = 160,
    Size = UDim2.fromOffset(450, 320),
    Acrylic = true,
    Theme = "Amethyst",
    MinimizeKey = Enum.KeyCode.End
})

-- Bật/Tắt Menu khi chạm nút
ImageButton.MouseButton1Click:Connect(function()
    Window:Minimize()
end)

local Tabs = {}

-- [[ 3. TAB THÔNG TIN (LUÔN CÓ Ở MỌI GAME) ]] --
Tabs.Info = Window:AddTab({ Title = "Thông Tin", Icon = "info" })
Tabs.Info:AddButton({
    Title = "Discord Community",
    Description = "Bấm để copy link Discord",
    Callback = function()
        setclipboard("https://discord.gg/tboyroblox-community-1253927333920899153")
        Fluent:Notify({ Title = "Hệ Thống", Content = "Đã copy link Discord!", Duration = 3 })
    end
})
Tabs.Info:AddButton({
    Title = "Kênh Youtube",
    Callback = function() setclipboard("https://www.youtube.com/@TBoyRoblox08") end
})

-- [[ 4. KIỂM TRA VÀ TẢI SCRIPT THEO GAME ]] --

-- KIỂM TRA BLOX FRUIT (Sea 1, 2, 3)
if PlaceID == 2753915549 or PlaceID == 4442272183 or PlaceID == 7449423635 then
    Tabs.BF = Window:AddTab({ Title = "Blox Fruits", Icon = "sword" })
    Tabs.BF:AddButton({
        Title = "Redz Hub",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/newredz/BloxFruits/refs/heads/main/Source.luau"))()
        end
    })
    Tabs.BF:AddButton({
        Title = "W-Azure Hub",
        Callback = function()
            loadstring(game:HttpGet("https://api.luarmor.net/files/v3/loaders/3b2169cf5333c0ffad8c01bc09311234.lua"))()
        end
    })

-- KIỂM TRA KING LEGACY (Tất cả Map)
elseif PlaceID == 3652625463 or PlaceID == 14455793425 or PlaceID == 16133333345 then
    Tabs.KL = Window:AddTab({ Title = "King Legacy", Icon = "crown" })
    Tabs.KL:AddButton({
        Title = "Banana Hub",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/BleuBlooker/BananaHub/main/KingLegacy.lua"))()
        end
    })
    Tabs.KL:AddButton({
        Title = "Auto Farm (Gọn Nhẹ)",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/XeroHub/XeroHub/main/KingLegacy.lua"))()
        end
    })

-- KIỂM TRA FISCH (CÂU CÁ)
elseif PlaceID == 16732694052 then
    Tabs.Fisch = Window:AddTab({ Title = "Fisch", Icon = "fish" })
    Tabs.Fisch:AddButton({
        Title = "CFrame Hub",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/CFrame360/Fisch/main/Script.lua"))()
        end
    })

-- NẾU LÀ GAME KHÔNG CÓ TRONG DANH SÁCH TRÊN
else
    Tabs.Other = Window:AddTab({ Title = "Không Hỗ Trợ", Icon = "clock" })
    Tabs.Other:AddParagraph({
        Title = "Thông Báo",
        Content = "Game này hiện chưa có Script trong hệ thống tổng hợp.\nID Game: " .. PlaceID
    })
    Tabs.Other:AddButton({
        Title = "Chạy Infinite Yield (Admin Lệnh)",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source"))()
        end
    })
end

-- Mặc định mở Tab Thông Tin
Window:SelectTab(1)

-- Thông báo khi script chạy xong
Fluent:Notify({
    Title = "6_7 Roblox",
    Content = "Script đã tải xong. Bấm nút đen để ẩn/hiện!",
    Duration = 5
})
