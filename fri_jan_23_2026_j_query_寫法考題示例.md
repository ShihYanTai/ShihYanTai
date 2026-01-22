# Copilot Chat Conversation Export: jQuery 寫法考題示例

**User:** @ShihYanTai
**Thread URL:** https://github.com/copilot/c/63cb05e2-4ba2-44c7-b492-b44baf2b6c1e

## @ShihYanTai

這職缺我需要面試當天手寫。

## Copilot

了解。因為你說「面試當天需要手寫」，重點會是：**不用 IDE / 不靠自動補全**、在白板或紙上把**思路與正確性**寫清楚。

不

## @ShihYanTai

這職缺我需要面試當天手寫，筆試科目：網頁程式設計　(約30分鐘) 。
軟體開發工程師01/12更新
南亞科技股份有限公司本公司其他工作
1 天內聯絡過求職者
徵才積極度：非常活躍
01/06已應徵
應徵人數 11~30 人
工作內容
1.網頁應用程式開發設計
2.系統管理及維護
3.專案規劃與分析
4.人工智慧方向相關應用(Machine learning/Deep learning/RAG/LLM)

職務類別
軟體工程師、前端工程師、資料工程師
工作待遇
待遇面議（經常性薪資達 4 萬元或以上）
工作性質
全職
上班地點
新北市泰山區南林路98號
管理責任
不需負擔管理責任
出差外派
無需出差外派
上班時段
日班
08:00~17:00
休假制度
週休二日
可上班日
一個月內
需求人數
1人
條件要求
工作經歷
不拘
學歷要求
大學、碩士
科系要求
資訊工程相關
語文條件
英文 -- 聽 /中等、說 /中等、讀 /中等、寫 /中等

提升英文能力
擅長工具
Visual Basic .net、Visual C#、Visual Studio .net、ADO、MySQL、Oracle、ActiveX、DHTML、VBScript、jQuery、Node.js
提升專業能力
工作技能
系統架構規劃、系統維護操作
其他條件
1.熟VB.NET、ASP.NET、HTML或C#等語言，且對網頁開發技術有所了解。  
2.擁有應用程式或報表開發的經驗，並熟悉使用關聯性資料庫、SQL語言。

## Copilot

你這個 30 分鐘「網頁程式設計」手寫筆試，依職缺工具鏈（VB.NET / C#、ASP.NET、HTML/JS、jQuery、Node.js、MySQL/Oracle、ADO）來看，最常考的不是花俏框架，而是：

- **HTTP/表單/CRUD 基本功**
- **SQL 查詢與資料處理**
- **資安與輸入驗證（XSS/SQL Injection）**
- **前後端串接的觀念（request/response、JSON）**
- 可能加一點 **基礎演算法/資料結構**（但會包裝成網頁情境）

下面我給你一套「30 分鐘手寫高命中準備法」：含**會考題型清單 + 你手寫時的標準模板 + 10 題練習題**。你照這個練 2~3 天，命中率會很高。

---

## 1) 30 分鐘筆試最可能長什麼樣（依這職缺）
### A. 小型 CRUD（最高機率）
題目：做一個「員工查詢 / 新增 / 修改 / 刪除」或「留言板」  
你要能手寫：
- HTML 表單（input/select）
- 後端接收（ASP.NET MVC / WebForms / 或 Node.js/Express 擇一）
- SQL（SELECT/INSERT/UPDATE/DELETE）
- 回傳結果（HTML 或 JSON）

### B. SQL + 資料庫題（第二高）
考：
- JOIN、GROUP BY、HAVING
- 查「最近一次」、「每人最新一筆」、「Top N」
- 基本索引觀念（口述即可）

### C. 前端 JS/jQuery + AJAX
考：
- 用 jQuery `$.ajax` / `fetch` 呼叫 API
- 表單驗證（必填、格式）
- DOM 操作（把回傳資料塞到 table）

### D. Web 基礎觀念問答（穿插）
- GET vs POST
- Cookie/Session
- RESTful 基本路由命名
- XSS / SQL Injection 怎麼防

---

## 2) 手寫拿高分的「固定寫法模板」（強烈建議背起來）
面試官看手寫，最怕你寫一堆零散片段。你用下面結構，會顯得很會做專案。

### 模板：題目是「查詢 + 新增」示例架構
1. **資料表設計（簡短）**
   - Employee(Id, Name, Dept, CreatedAt)

2. **API/路由**
   - `GET /employees?dept=IT`
   - `POST /employees` body: `{name, dept}`

3. **SQL**
   - 查詢：`SELECT ... WHERE ... ORDER BY ...`
   - 新增：`INSERT INTO ...`

4. **後端程式（一定寫參數化查詢）**
   - 連線字串
   - 參數 `@dept`, `@name`
   - try/catch、回傳結果

5. **前端（HTML + JS）**
   - 表單
   - AJAX 呼叫
   - render table

6. **資安加分句（必寫一行）**
   - 「使用參數化查詢避免 SQL Injection」
   - 「輸出做 HTML encode 避免 XSS」

---

## 3) 你該選哪個語言手寫？（依公司偏好）
從工具列看起來他們偏 **.NET**。你如果會 C#，建議手寫用：

- **ASP.NET MVC/Web API 風格**（Controller + Model）
- DB 用 **ADO.NET**（SqlConnection / SqlCommand / parameters）

因為職缺寫了 ADO、VB.NET、C#，用 ADO.NET 參數化查詢會非常對味。

如果你更熟 Node.js，也可以用 Express，但**這家公司比較像傳統 MIS/.NET**，手寫 C# 通常更討喜。

---

## 4) 高命中練習題（你可以計時 30 分鐘寫）
你先挑 3~5 題練到熟。

### 題 1：會員登入（Web 基礎 + SQL + Session）
- 資料表：Users(Id, Account, PasswordHash)
- 寫：登入流程（POST /login），驗證成功後建立 Session

### 題 2：留言板查詢 + 新增（CRUD）
- Messages(Id, Author, Content, CreatedAt)
- `GET /messages`、`POST /messages`
- 前端用 AJAX 顯示列表

### 題 3：SQL：每個部門薪水最高的員工
- Emp(EmpId, Name, DeptId, Salary)
- Dept(DeptId, DeptName)
- 寫 SQL（JOIN + 子查詢 or window function）

### 題 4：AJAX：輸入工號即時查員工資料
- `GET /employee/{id}` 回 JSON
- 前端輸入框 change 時呼叫並顯示

### 題 5：防 SQL Injection（給一段錯誤程式叫你改）
- 把字串拼接改成 parameters

---

## 5) 我需要你補兩個資訊，才能幫你做「最像考題的 30 分鐘模擬卷」
1) 你面試筆試允許使用哪種語言？你比較熟 **C# / VB.NET / Node.js** 哪個？  
2) 他有說是偏 **前端(HTML/JS)**、**後端(ASP.NET/Node)**、還是 **SQL** 比重比較高嗎？（例如筆試範圍或歷屆題型）

你回我這兩點後，我可以直接給你一份：
- **30 分鐘模擬題（1 大題 + 2 小題）**
- **標準作答版面配置（手寫怎麼排版）**
- **常見扣分點清單**（例如忘了參數化、忘了 HTTP method 等）

## @ShihYanTai

1.比較熟 C# 
2.前端(HTML/JS)、後端(ASP.NET/Node)、基本 SQL 

## Copilot

好，那就用你最熟的 **C#**，用最容易手寫、也最貼這職缺的組合：**ASP.NET Core Web API + ADO.NET（參數化 SQL）+ 前端 HTML/JS（fetch）**。下面是一份很像真實筆試的 **30 分鐘模擬卷**，以及你手寫時照抄就能拿分的「版面模板」。

---

## 30 分鐘模擬卷（建議配置：20 分鐘大題 + 10 分鐘觀念/SQL）
### 大題：員工查詢 + 新增（API + SQL + 前端）
情境：建立一個簡易員工清單頁，能：
1. 依部門查詢員工（顯示在表格）
2. 新增員工（新增後重新載入列表）

資料表 `Employees`：

- `Id` INT (PK, identity)
- `Name` NVARCHAR(50)
- `Dept` NVARCHAR(50)
- `CreatedAt` DATETIME

需求：
- `GET /api/employees?dept=IT`：回傳 JSON 陣列
- `POST /api/employees`：body JSON `{ "name": "...", "dept": "..." }`，新增一筆後回傳 `{ id: 新id }`
- 前端 `index.html`：有 dept 查詢欄位、name/dept 新增表單、一個 table 顯示查詢結果
- 必須：**參數化查詢**避免 SQL Injection

---

## 你手寫答案的「標準排版」（照這順序寫最穩）
### 1) API Contract（先寫這段讓面試官秒懂）
- `GET /api/employees?dept={optional}` → `200 OK` `[{id,name,dept,createdAt}]`
- `POST /api/employees` body: `{name, dept}` → `201 Created` `{id}`

### 2) SQL（先列出查詢/新增的 SQL）
- 查詢（dept 可選）  
  - 若有 dept：  
    `SELECT Id, Name, Dept, CreatedAt FROM Employees WHERE Dept = @dept ORDER BY Id DESC;`
  - 若沒 dept：  
    `SELECT Id, Name, Dept, CreatedAt FROM Employees ORDER BY Id DESC;`

- 新增：  
  `INSERT INTO Employees(Name, Dept, CreatedAt) VALUES(@name, @dept, GETDATE()); SELECT SCOPE_IDENTITY();`

### 3) C# Web API（Controller + ADO.NET）
你可以手寫成這種「能看懂就得分」的精簡版本：

```csharp
// Model
public record CreateEmployeeDto(string Name, string Dept);

public class EmployeeRow {
    public int Id { get; set; }
    public string Name { get; set; }
    public string Dept { get; set; }
    public DateTime CreatedAt { get; set; }
}

// Controller (pseudo)
[ApiController]
[Route("api/[controller]")]
public class EmployeesController : ControllerBase
{
    private readonly string _connStr = "Server=...;Database=...;Trusted_Connection=True;";

    [HttpGet]
    public IActionResult Get([FromQuery] string? dept)
    {
        var list = new List<EmployeeRow>();

        using var conn = new SqlConnection(_connStr);
        conn.Open();

        string sql = string.IsNullOrWhiteSpace(dept)
            ? "SELECT Id, Name, Dept, CreatedAt FROM Employees ORDER BY Id DESC"
            : "SELECT Id, Name, Dept, CreatedAt FROM Employees WHERE Dept=@dept ORDER BY Id DESC";

        using var cmd = new SqlCommand(sql, conn);
        if (!string.IsNullOrWhiteSpace(dept))
            cmd.Parameters.AddWithValue("@dept", dept);

        using var reader = cmd.ExecuteReader();
        while (reader.Read())
        {
            list.Add(new EmployeeRow {
                Id = reader.GetInt32(0),
                Name = reader.GetString(1),
                Dept = reader.GetString(2),
                CreatedAt = reader.GetDateTime(3)
            });
        }

        return Ok(list);
    }

    [HttpPost]
    public IActionResult Create([FromBody] CreateEmployeeDto dto)
    {
        if (string.IsNullOrWhiteSpace(dto.Name) || string.IsNullOrWhiteSpace(dto.Dept))
            return BadRequest("Name/Dept required");

        using var conn = new SqlConnection(_connStr);
        conn.Open();

        string sql = @"INSERT INTO Employees(Name, Dept, CreatedAt)
                       VALUES(@name, @dept, GETDATE());
                       SELECT CAST(SCOPE_IDENTITY() as int);";

        using var cmd = new SqlCommand(sql, conn);
        cmd.Parameters.AddWithValue("@name", dto.Name);
        cmd.Parameters.AddWithValue("@dept", dto.Dept);

        int newId = (int)cmd.ExecuteScalar();
        return StatusCode(201, new { id = newId });
    }
}
```

手寫加分句（寫在旁邊一行即可）：
- 「用 `cmd.Parameters` 做**參數化查詢**避免 SQL Injection」
- 「輸出到 HTML 時要 encode 避免 XSS（若直接 innerHTML）」

### 4) 前端 HTML + JS（fetch + render table）
手寫不用很完整，但要有結構：輸入、按鈕、table、fetch、render。

```html
<input id="deptQuery" placeholder="dept e.g. IT">
<button onclick="load()">Search</button>

<h3>Add</h3>
<input id="name" placeholder="name">
<input id="dept" placeholder="dept">
<button onclick="add()">Add</button>

<table border="1">
  <thead><tr><th>Id</th><th>Name</th><th>Dept</th><th>CreatedAt</th></tr></thead>
  <tbody id="tbody"></tbody>
</table>

<script>
async function load() {
  const dept = document.getElementById('deptQuery').value.trim();
  const url = dept ? `/api/employees?dept=${encodeURIComponent(dept)}` : `/api/employees`;
  const res = await fetch(url);
  const data = await res.json();

  const tbody = document.getElementById('tbody');
  tbody.innerHTML = data.map(e =>
    `<tr><td>${e.id}</td><td>${e.name}</td><td>${e.dept}</td><td>${e.createdAt}</td></tr>`
  ).join('');
}

async function add() {
  const name = document.getElementById('name').value.trim();
  const dept = document.getElementById('dept').value.trim();

  await fetch('/api/employees', {
    method: 'POST',
    headers: {'Content-Type':'application/json'},
    body: JSON.stringify({ name, dept })
  });

  await load();
}
</script>
```

（如果你想更安全，可補一句：避免用 innerHTML 直接塞使用者輸入，或要 escape。）

---

## 10 分鐘小題（常見觀念 + SQL）
你可以在大題寫完後快速補這些，通常會送分：

### 小題 1：GET vs POST 差異（寫 3 點）
- GET：用於查詢、參數在 URL、可被快取/書籤、通常不放敏感資料  
- POST：用於新增/修改、資料在 body、不可書籤、適合送表單/JSON  
- 兩者都走 HTTP，但語意不同（REST）

### 小題 2：寫一個基本 SQL（查 IT 部門最新 10 筆）
```sql
SELECT TOP 10 Id, Name, Dept, CreatedAt
FROM Employees
WHERE Dept = @dept
ORDER BY CreatedAt DESC;
```

（MySQL 版本就 `LIMIT 10`，但這職缺偏 MSSQL/Oracle 也合理。）

---

## 最容易扣分的 6 個點（你上場前記一下）
1) SQL 用字串拼接（直接扣資安分）→ 一律 parameters  
2) 忘記處理 dept 可能為空 → 兩段 SQL 或動態條件  
3) 忘記 `Content-Type: application/json` → POST 常被認為不完整  
4) 忘記回傳格式（JSON/HTTP status）→ 至少寫 `Ok(...)` / `201`  
5) 前端查詢沒 `encodeURIComponent` → 參數有空白會壞  
6) CreatedAt 用程式端產生也行，但寫 `GETDATE()` 最省

---

如果你願意，我也可以再幫你做「更貼近實戰」的第二套題目（可能是**登入 + Session + SQL**，或**查詢+分頁+排序**）。你想公司更偏 **傳統 MIS 報表/CRUD**，還是偏 **API + 前端互動**？

## @ShihYanTai

請幫我提供jQuery 寫法考題

## Copilot

下面給你一份很像 30 分鐘筆試會出的 **jQuery 寫法考題（含題目 + 參考解）**。你可以先遮住參考解自己寫一遍，練到「不用查語法」就穩了。

---

## 考題（jQuery + AJAX + DOM + 表單驗證）
情境：做一個「員工查詢與新增」頁面（不需後端實作，但要能呼叫 API）。

### 已知 API
1. `GET /api/employees?dept=IT`  
回傳：
```json
[
  {"id":1,"name":"Amy","dept":"IT","createdAt":"2026-01-18T09:00:00"},
  {"id":2,"name":"Bob","dept":"IT","createdAt":"2026-01-18T10:00:00"}
]
```

2. `POST /api/employees`，Content-Type: application/json  
body:
```json
{"name":"Chris","dept":"HR"}
```
成功回傳：
```json
{"id": 100}
```

### 題目要求（手寫）
請用 **jQuery** 完成以下功能：

1) 畫面載入時自動呼叫 `GET /api/employees`，把結果顯示在 table（`#empTbody`）  
2) 點擊「查詢」按鈕（`#btnSearch`）時：  
- 讀取 `#deptQuery` 的值  
- 組出查詢 URL（dept 有填才帶參數）  
- 呼叫 GET 並更新 table  
3) 點擊「新增」按鈕（`#btnAdd`）時：  
- 讀取 `#name`、`#dept`  
- 前端驗證：任一空白就 `alert("Name/Dept required")` 並 return  
- 用 `$.ajax` POST JSON 到 `/api/employees`  
- 成功後清空輸入框並重新查詢列表  
4) 額外加分：AJAX 發生錯誤時顯示 `alert("error")`

HTML 已提供（不可改 id）：

```html
<input id="deptQuery" placeholder="dept (optional)">
<button id="btnSearch">Search</button>

<hr>

<input id="name" placeholder="name">
<input id="dept" placeholder="dept">
<button id="btnAdd">Add</button>

<table border="1">
  <thead>
    <tr><th>Id</th><th>Name</th><th>Dept</th><th>CreatedAt</th></tr>
  </thead>
  <tbody id="empTbody"></tbody>
</table>
```

---

## 參考解（jQuery 標準寫法，筆試手寫版本）
你手寫時可以把它分成：事件綁定、共用函式 load、render。

```javascript
$(function () {
  // page ready
  loadEmployees();

  $("#btnSearch").on("click", function () {
    loadEmployees();
  });

  $("#btnAdd").on("click", function () {
    addEmployee();
  });
});

function loadEmployees() {
  var dept = $.trim($("#deptQuery").val());
  var url = "/api/employees";
  if (dept !== "") {
    url += "?dept=" + encodeURIComponent(dept);
  }

  $.getJSON(url)
    .done(function (data) {
      renderTable(data);
    })
    .fail(function () {
      alert("error");
    });
}

function renderTable(data) {
  var rows = "";
  $.each(data, function (i, e) {
    rows += "<tr>"
      + "<td>" + e.id + "</td>"
      + "<td>" + e.name + "</td>"
      + "<td>" + e.dept + "</td>"
      + "<td>" + e.createdAt + "</td>"
      + "</tr>";
  });
  $("#empTbody").html(rows);
}

function addEmployee() {
  var name = $.trim($("#name").val());
  var dept = $.trim($("#dept").val());

  if (name === "" || dept === "") {
    alert("Name/Dept required");
    return;
  }

  $.ajax({
    url: "/api/employees",
    method: "POST",
    contentType: "application/json; charset=utf-8",
    data: JSON.stringify({ name: name, dept: dept })
  })
  .done(function (res) {
    $("#name").val("");
    $("#dept").val("");
    loadEmployees();
  })
  .fail(function () {
    alert("error");
  });
}
```

---

## 面試官常看的「關鍵得分點」
- 有用 `$(function(){ ... })` 或 `$(document).ready(...)`
- GET 用 `$.getJSON` 或 `$.ajax({method:"GET"})`
- POST 有寫 `contentType: "application/json"` + `JSON.stringify`
- 參數有 `encodeURIComponent`
- DOM 更新用 `$("#empTbody").html(rows)`
- `fail`/`error` 有處理

---

如果你想更貼筆試，我也可以再給你第二題：**即時搜尋（keyup debounce）+ 只更新指定列 + 顯示 loading**，這種也很常考。你想偏「基本 CRUD」還是「互動題（keyup/動態新增列/事件委派）」？

## @ShihYanTai

給我Javascript 基礎知識如list 或json 取值順序，有些筆試會考的相關模擬考

## Copilot

以下是偏「筆試會考、而且要手寫」的 **JavaScript 基礎知識重點 + 模擬考題**（含答案）。我會特別放你提到的 **list/JSON 取值、順序**，以及常見的 **型別、== vs ===、scope、this、async** 等。

---

## 一、你要先記住的核心觀念（考很兇）

### 1) Array（list）順序
- Array 是**有序**集合，索引從 0 開始。
- `push` 加在尾端；`pop` 從尾端拿；`shift` 從頭拿；`unshift` 加在頭。
- `for...of`：依 array 的順序跑值  
- `forEach`：依序跑 callback（但不能 `break`）

### 2) Object / JSON 的「順序」陷阱
- JSON 是字串格式；parse 後變成 JS object。
- **Object 本質是 key-value，不應依賴順序**。
- 但現代 JS 對「列舉順序」有規則（筆試很愛陰你）：
  1. **整數型 key（像 "0","1","2"）會先依數字升冪**
  2. 其他字串 key 依**插入順序**
  3. Symbol keys 最後
- 結論（手寫答題建議）：  
  - **Array 才保證順序**  
  - Object 的 key 順序「不要依賴」，需要順序就用 Array 或明確排序 `Object.keys(obj).sort()`。

### 3) 取值方式
- Array：`arr[i]`
- Object：`obj.key` 或 `obj["key"]`
  - key 不是合法識別字（如 `user-name`）或是變數時，一定要 `obj[k]`

### 4) `==` vs `===`
- `===` 不做型別轉換（筆試通常建議用它）
- `==` 會做型別轉換，容易踩雷：`"0" == 0` 為 true

### 5) `var` / `let` / `const`
- `var`：function scope，會 hoist（宣告提升），容易出坑  
- `let/const`：block scope，有 TDZ（暫時死區）  
- `const`：不能重新指派，但物件內容仍可改（`const obj = {}; obj.a=1` OK）

### 6) 淺拷貝 vs 深拷貝（常考）
- `obj2 = obj1`：只是同一個參考
- 淺拷貝：`{...obj}`、`arr.slice()`、`[...arr]`
- 深拷貝（簡化版）：`structuredClone(obj)`（新）或 `JSON.parse(JSON.stringify(obj))`（有侷限：Date/function/undefined 會壞）

### 7) Promise/async 的執行順序（事件迴圈）
- 同步程式碼先跑完
- `Promise.then`（microtask）通常比 `setTimeout`（macrotask）早執行

---

## 二、模擬考（JS 基礎手寫）— 15 題

### Q1（Array 順序）
```js
let a = [1,2];
a.push(3);
a.unshift(0);
a.pop();
console.log(a);
```
答案：`[0,1,2]`

---

### Q2（Object vs Array 取值）
```js
const obj = { name: "Amy", 0: "zero", 1: "one" };
console.log(obj[0], obj["name"]);
```
答案：`"zero" "Amy"`

---

### Q3（Object 列舉順序陷阱）
```js
const o = {};
o["b"] = 1;
o["10"] = 2;
o["2"] = 3;
o["a"] = 4;
console.log(Object.keys(o));
```
答案（重點）：整數型 key 先升冪，再字串插入順序  
`["2","10","b","a"]`

---

### Q4（JSON parse 後取值）
```js
const s = '{"user":{"name":"Bob","skills":["js","sql"]}}';
const data = JSON.parse(s);
console.log(data.user.skills[1]);
```
答案：`"sql"`

---

### Q5（for...in vs for...of）
```js
const arr = ["a","b"];
for (const i in arr) console.log(i);
for (const v of arr) console.log(v);
```
答案：  
`for...in` 印索引：`0 1`  
`for...of` 印值：`a b`

---

### Q6（== vs ===）
```js
console.log("0" == 0);
console.log("0" === 0);
console.log(null == undefined);
console.log(null === undefined);
```
答案：
- `"0" == 0` → `true`
- `"0" === 0` → `false`
- `null == undefined` → `true`
- `null === undefined` → `false`

---

### Q7（NaN 特性）
```js
console.log(NaN === NaN);
console.log(Number.isNaN(NaN));
```
答案：
- `false`
- `true`

---

### Q8（var hoisting）
```js
console.log(x);
var x = 5;
console.log(x);
```
答案：
- 第一行 `undefined`（宣告提升，值未指派）
- 第二行 `5`

---

### Q9（let TDZ）
```js
console.log(y);
let y = 5;
```
答案：會丟錯（ReferenceError），因為 TDZ

---

### Q10（const 物件可改內容）
```js
const u = { name: "Amy" };
u.name = "Bea";
console.log(u.name);
```
答案：`"Bea"`

---

### Q11（淺拷貝陷阱）
```js
const a1 = [{x:1}];
const a2 = a1.slice();
a2[0].x = 9;
console.log(a1[0].x);
```
答案：`9`（slice 只拷貝陣列殼，裡面物件仍同參考）

---

### Q12（展開運算子：淺拷貝）
```js
const o1 = { a:1, nested:{ b:2 } };
const o2 = { ...o1 };
o2.nested.b = 99;
console.log(o1.nested.b);
```
答案：`99`（nested 仍共用）

---

### Q13（this：一般函式 vs arrow）
```js
const obj = {
  val: 1,
  f: function() { return this.val; },
  g: () => this.val
};
console.log(obj.f());
console.log(obj.g());
```
答案：
- `obj.f()` → `1`
- `obj.g()` → 多半是 `undefined`（arrow 的 this 不是 obj，而是外層 this）

---

### Q14（閉包：常見筆試）
```js
function makeCounter() {
  let c = 0;
  return function() { c++; return c; }
}
const inc = makeCounter();
console.log(inc());
console.log(inc());
```
答案：
- `1`
- `2`

---

### Q15（事件迴圈順序：Promise vs setTimeout）
```js
console.log(1);
setTimeout(() => console.log(2), 0);
Promise.resolve().then(() => console.log(3));
console.log(4);
```
答案順序：`1 4 3 2`

---

## 三、加碼：常見「手寫題型」2 題（偏實作）
這種題目很常出現在 30 分鐘筆試最後一題。

### 實作題 A：把 API 回傳資料轉成部門統計
給：
```js
const employees = [
  {name:"Amy", dept:"IT"},
  {name:"Bob", dept:"IT"},
  {name:"Chris", dept:"HR"}
];
```
要求輸出：
```js
{ IT: 2, HR: 1 }
```

參考解（手寫版）：
```js
const countByDept = {};
for (const e of employees) {
  const d = e.dept;
  countByDept[d] = (countByDept[d] || 0) + 1;
}
```

### 實作題 B：安全取值（避免 undefined 爆掉）
給：
```js
const data = { user: { profile: { email: "a@b.com" } } };
```
要求：取出 email，如果不存在回傳空字串。

參考解：
```js
const email = data?.user?.profile?.email ?? "";
```

---

你想把模擬考更貼近「網頁程式設計」一點嗎？例如我可以再出一份：  
- **jQuery + AJAX + JSON 解析 + 表格渲染** 的 30 分鐘整卷（含錯誤除錯題），會更像你面試當天的筆試格式。

## @ShihYanTai

jQuery + AJAX + JSON 解析 + 表格渲染

## Copilot

## 30 分鐘模擬卷：jQuery + AJAX + JSON 解析 + 表格渲染（含除錯題）
建議時間：  
- 第 1 題（主題 CRUD + 表格渲染）：20 分鐘  
- 第 2 題（除錯題）：5 分鐘  
- 第 3 題（觀念題）：5 分鐘

---

# 第 1 題（主題實作題，20 分）
你要完成一個「員工清單」頁面，具備：
- 查詢（依部門 dept）
- 新增（name、dept）
- 用 AJAX 拿 JSON 後渲染到 table
- 要處理錯誤、顯示 loading

### 已知 API（不用寫後端）
1) `GET /api/employees?dept=IT`（dept 可省略）  
回傳 JSON（陣列）：
```json
[
  {"id":1,"name":"Amy","dept":"IT","createdAt":"2026-01-18T09:00:00"},
  {"id":2,"name":"Bob","dept":"IT","createdAt":"2026-01-18T10:00:00"}
]
```

2) `POST /api/employees`，Content-Type: application/json  
送出：
```json
{"name":"Chris","dept":"HR"}
```
成功回傳：
```json
{"id": 100}
```

---

## HTML（題目給定，不可改 id）
你只需要寫 `<script>` 的 jQuery 程式。

```html
<input id="deptQuery" placeholder="dept (optional)">
<button id="btnSearch">Search</button>
<span id="loading" style="display:none;">Loading...</span>

<hr>

<input id="name" placeholder="name">
<input id="dept" placeholder="dept">
<button id="btnAdd">Add</button>

<table border="1" width="600">
  <thead>
    <tr><th>Id</th><th>Name</th><th>Dept</th><th>CreatedAt</th></tr>
  </thead>
  <tbody id="empTbody"></tbody>
</table>

<div id="msg" style="color:red;"></div>
```

---

## 需求（你要用 jQuery 完成）
A. 頁面載入完成後，自動查詢一次（不帶 dept）並渲染 table  
B. 點 `#btnSearch` 時：
- 讀取 `#deptQuery`（trim）
- dept 有值才組 query string，且要 `encodeURIComponent`
- AJAX GET 成功後渲染 table

C. 點 `#btnAdd` 時：
- 讀取 `#name`、`#dept`（trim）
- 若任一空白：在 `#msg` 顯示 `"Name/Dept required"` 並 return
- AJAX POST JSON（`contentType: "application/json"`、`data: JSON.stringify(...)`）
- 成功後清空輸入框、清空錯誤訊息、再觸發查詢刷新列表

D. Loading：
- 發送 AJAX 前顯示 `#loading`
- 完成（成功或失敗）後隱藏 `#loading`

E. 表格渲染：
- 把回傳的陣列渲染成 `<tr>` 列表塞到 `#empTbody`
- 若回傳陣列為空：顯示一列 `No data`

F. 錯誤處理：
- 任何 AJAX 失敗：在 `#msg` 顯示 `"Request failed"`

---

# 第 2 題（除錯題，5 分）
以下程式碼想做「查詢後渲染」，但有 4 個錯誤，請指出並改正：

```js
$("#btnSearch").click(function () {
  var dept = $("#deptQuery").val();
  $.ajax({
    url: "/api/employees?dept=" + dept,
    method: "GET",
    dataType: "json"
  }).done(function (data) {
    var rows;
    data.forEach(function (e) {
      rows += "<tr><td>" + e.Id + "</td><td>" + e.Name + "</td></tr>";
    });
    $("#empTbody").text(rows);
  });
});
```

---

# 第 3 題（觀念題，5 分）
1) `dataType: "json"` 與 `contentType: "application/json"` 差在哪？  
2) 為什麼 query string 要用 `encodeURIComponent`？

---

---

## 參考解（建議你先自己寫再對答案）

### 第 1 題參考解（jQuery + AJAX + render）
```javascript
$(function () {
  // page load
  loadEmployees();

  $("#btnSearch").on("click", function () {
    loadEmployees();
  });

  $("#btnAdd").on("click", function () {
    addEmployee();
  });
});

function showLoading(show) {
  if (show) $("#loading").show();
  else $("#loading").hide();
}

function setMsg(text) {
  $("#msg").text(text || "");
}

function buildQueryUrl() {
  var dept = $.trim($("#deptQuery").val());
  var url = "/api/employees";
  if (dept !== "") {
    url += "?dept=" + encodeURIComponent(dept);
  }
  return url;
}

function loadEmployees() {
  setMsg("");
  showLoading(true);

  $.ajax({
    url: buildQueryUrl(),
    method: "GET",
    dataType: "json" // expect JSON from server
  })
  .done(function (data) {
    renderTable(data);
  })
  .fail(function () {
    setMsg("Request failed");
  })
  .always(function () {
    showLoading(false);
  });
}

function renderTable(data) {
  var rows = "";

  if (!data || data.length === 0) {
    rows = "<tr><td colspan='4'>No data</td></tr>";
    $("#empTbody").html(rows);
    return;
  }

  $.each(data, function (i, e) {
    rows += "<tr>"
      + "<td>" + e.id + "</td>"
      + "<td>" + e.name + "</td>"
      + "<td>" + e.dept + "</td>"
      + "<td>" + e.createdAt + "</td>"
      + "</tr>";
  });

  $("#empTbody").html(rows);
}

function addEmployee() {
  var name = $.trim($("#name").val());
  var dept = $.trim($("#dept").val());

  if (name === "" || dept === "") {
    setMsg("Name/Dept required");
    return;
  }

  setMsg("");
  showLoading(true);

  $.ajax({
    url: "/api/employees",
    method: "POST",
    contentType: "application/json; charset=utf-8", // send JSON
    dataType: "json", // expect JSON response: {id:...}
    data: JSON.stringify({ name: name, dept: dept })
  })
  .done(function (res) {
    $("#name").val("");
    $("#dept").val("");
    loadEmployees();
  })
  .fail(function () {
    setMsg("Request failed");
  })
  .always(function () {
    showLoading(false);
  });
}
```

> 手寫加分點：  
> - `always()` 確保 loading 一定關掉  
> - query string 有 `encodeURIComponent`  
> - 用 `.html()` 更新表格（不是 `.text()`）

---

### 第 2 題除錯題解答（4 個錯）
原碼問題點與修正：

1) `dept` 沒 trim、也沒 encode → 需要：
```js
var dept = $.trim($("#deptQuery").val());
var url = "/api/employees";
if (dept !== "") url += "?dept=" + encodeURIComponent(dept);
```

2) `var rows;` 沒初始化，會變成 `undefined...` → 改：
```js
var rows = "";
```

3) JSON 欄位大小寫錯：回傳是 `id/name`，不是 `Id/Name` → 改：
```js
e.id, e.name
```

4) 更新 tbody 用 `.text(rows)` 會把 HTML 當文字 → 要用 `.html(rows)`：
```js
$("#empTbody").html(rows);
```

（可加分的第 5 點：沒處理 fail/always、dept 空值情況。）

---

### 第 3 題觀念題解答
1) 差異：
- `dataType: "json"`：告訴 jQuery「**回應**要用 JSON 解析」
- `contentType: "application/json"`：告訴伺服器「我送出去的 **request body** 是 JSON」

2) `encodeURIComponent` 原因：
- 避免空白、&、?、中文等特殊字元破壞 URL
- 防止 query string 被截斷或解析錯誤（例如 dept=`R&D`）

---

如果你要我再出一份「更像公司 MIS 的」版本，我可以改成：**查詢(含關鍵字) + 分頁 + 點列選取顯示明細**，這種也超常考。你想加上「點某列顯示詳細資料」嗎？
