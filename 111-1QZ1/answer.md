# 第1次隨堂-隨堂-QZ1
>
>學號：108111121
><br />
>姓名：郭柏葳 
><br />
>作業撰寫時間：50 (mins，包含程式撰寫時間)
><br />
>最後撰寫文件日期：2022/9/27
>

本份文件包含以下主題：(至少需下面兩項，若是有多者可以自行新增)
- [x]說明內容
- [x]個人認為完成作業須具備觀念

## 說明程式與內容
生成一個整數2維陣列變數大小為10* 10，名稱為ia_Map。
生成一個整數1維陣列變數大小為10，名稱為ia_MIndex
讓地雷儲存在ia_MIndex 隨機生成 0-99之中


```csharp
    public partial class Bomb : System.Web.UI.Page
    {
        protected void Page_Load(object sender, EventArgs e)
        {
            int[] ia_Mlndex = new int[10] { 0, 7, 13, 28, 44, 62, 74, 75, 87, 90 };
            char[,] ia_Map = new char[10, 10];
            for(int i_Row = 0; i_Row < 10; i_Row++)
            {
                for (int i_Col = 0; i_Col < 10; i_Col++)
                {
                    ia_Map[i_Row, i_Col] = "0";
                }
            }   
            for(int i_Ct = 0; i_Ct <10; i_Ct++)
            {
                int i_Row = ia_Mlndex / 10;
                int i_Col = ia_Mlndex % 10;
                ia_Map[i_Row i_Col] = "*";
            }
            /*尋訪2D array*/
            for(int i_Row = 0; i_Row < 10; i_Row++)
            {
                for(int i_Col = 0; i_Col < 10; i_Col++)
                {
                    if (ia_Map[i_Row, i_Col] == '') {
                        Response.Write("&nbsp;");
                    }
                    else { 
                    }
                    Response.Write(ia_Map[i_Row, i_Col]);
                }
            }
            Response.Write("<br />");
        }
    }

若要於內文中標示部分.aspx檔，則使用以下標籤` ```html 程式碼 ``` `，
下段程式碼則為使用後結果：

```html
<%@ Page Language="C#" AutoEventWireup="true" ...>

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
<meta http-equiv="Content-Type" ...>
    <title></title>
</head>
<body>
    <form id="form1" runat="server">
        <div>
        </div>
    </form>
</body>
</html>
```


## 個人認為完成作業須具備觀念
需有接觸過踩地雷的遊戲，以及對矩陣的基本觀念和正確使用方式，稍微進階一點的程式語言使用EX:for跟if的使用方式

