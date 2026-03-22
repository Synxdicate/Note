# หลักสูตรการเงินฉบับสมบูรณ์ — จากพื้นฐานสู่ความมั่งคั่ง

ผมดีใจมากที่คุณถามคำถามนี้ตอนที่ยังอายุน้อย เพราะสิ่งที่มีค่าที่สุดในการสร้างความมั่งคั่งไม่ใช่เงิน แต่คือ **เวลา** และคุณมีมันอยู่มากกว่าใครในห้อง ก่อนที่เราจะเข้าสู่รายการหัวข้อ ผมอยากให้คุณเข้าใจโครงสร้างก่อน เพราะการเรียนการเงินโดยไม่รู้ว่าแต่ละเรื่องเชื่อมกันอย่างไร เหมือนกับการเรียน Data Structure โดยไม่รู้ว่ามันจะถูกใช้ใน Algorithm ตัวไหน — คุณจะจำได้แต่ลืมความหมาย

---

## ภาพรวมโครงสร้างความรู้ทางการเงิน

ผมแบ่งความรู้ทั้งหมดออกเป็น **4 ชั้น** โดยเรียงจากรากฐานขึ้นไปสู่ยอด เหมือนกับการ build โปรแกรม คุณต้องเข้าใจ logic ก่อนจะเขียน function และต้องเขียน function ก่อนจะ deploy system ใหญ่ได้

---

## ชั้นที่ 1 — รากฐาน: Personal Finance & Financial Literacy

- Personal Budgeting และ Cash Flow Management
- Emergency Fund และ Liquidity Planning
- Time Value of Money (TVM) — แนวคิดว่าเงิน 100 บาทวันนี้มีค่ามากกว่า 100 บาทในอนาคต
- Compound Interest — กลไกที่ Einstein เรียกว่า "the eighth wonder of the world"
- Debt Management — ความต่างระหว่าง Good Debt และ Bad Debt
- Credit Score และ Credit History
- Insurance Basics — ประกันชีวิต ประกันสุขภาพ ประกันทรัพย์สิน
- Basic Accounting Concepts — งบกำไรขาดทุน งบดุล และ Cash Flow Statement

> **ทำไมชั้นนี้ถึงสำคัญที่สุด?** เพราะนักลงทุนที่เก่งที่สุดในโลกก็ยังล้มเหลวได้ถ้าเขาไม่มี financial discipline ในชีวิตส่วนตัว Warren Buffett เองยังบอกว่า "Do not save what is left after spending, but spend what is left after saving." ชั้นนี้คือ OS ของระบบการเงินคุณ ทุกอย่างรันอยู่บนมัน

---

## ชั้นที่ 2 — ภาษีและกฎหมาย: Tax & Regulatory Knowledge

- ระบบภาษีเงินได้บุคคลธรรมดาในประเทศไทย (ภงด.91 และ ภงด.90)
- ภาษีจากการลงทุน — Capital Gains Tax, Dividend Tax, และ Withholding Tax
- การลดหย่อนภาษีที่นักลงทุนควรรู้ — LTF/RMF (หรือ SSF/RMF ในปัจจุบัน), กองทุนสำรองเลี้ยงชีพ (PVD)
- ภาษีจากการลงทุนในต่างประเทศ — เช่น ถ้าคุณซื้อหุ้น US ผ่าน Webull หรือ Interactive Brokers มีภาษีอะไรที่เกี่ยวข้องบ้าง
- Estate Planning เบื้องต้น — การวางแผนมรดกและภาษีมรดก
- กฎระเบียบของ กลต. (SEC ประเทศไทย) และข้อบังคับการลงทุน

> **Mental Exercise สำหรับคุณ:** ลองถามตัวเองว่า ถ้าคุณได้เงินปันผลมา 10,000 บาทจากกองทุนรวม กับ 10,000 บาทจากการขายหุ้นที่กำไร คุณเสียภาษีเท่ากันไหม? คำตอบคือไม่เท่ากัน และนี่คือเหตุผลที่คุณต้องเรียนชั้นนี้

---

## ชั้นที่ 3 — การลงทุน: Investment Knowledge

### 3.1 เครื่องมือการลงทุนพื้นฐาน (Asset Classes)

- **ตราสารทุน (Equities)** — หุ้นสามัญ หุ้นบุริมสิทธิ์ และ ETF
- **ตราสารหนี้ (Fixed Income)** — พันธบัตรรัฐบาล หุ้นกู้ และ Duration Risk
- **อสังหาริมทรัพย์ (Real Estate)** — REIT คืออะไร และทำไมถึงสำคัญสำหรับนักลงทุนรายย่อย
- **สินค้าโภคภัณฑ์ (Commodities)** — ทองคำ น้ำมัน และบทบาทของมันใน Portfolio
- **Derivatives** — Options, Futures, Warrants และ DW (Derivative Warrants ในไทย)
- **Alternative Investments** — Private Equity, Venture Capital, Cryptocurrency
- **กองทุนรวม (Mutual Funds)** — ความแตกต่างระหว่าง Active vs. Passive Fund

### 3.2 การวิเคราะห์หลักทรัพย์ (Security Analysis)

- **Fundamental Analysis** — การอ่านและตีความงบการเงิน, Financial Ratios เช่น P/E, P/B, ROE, Debt-to-Equity
- **Technical Analysis** — Price Action, Moving Averages, RSI, MACD, Bollinger Bands
- **Quantitative Analysis** — Statistical Models, Factor Models, Backtesting (นี่คือจุดที่ CS ของคุณจะส่องแสง)
- **Valuation Methods** — DCF (Discounted Cash Flow), Comparable Company Analysis

### 3.3 Portfolio Theory

- Modern Portfolio Theory (Markowitz) — Efficient Frontier และการหา Optimal Portfolio
- Capital Asset Pricing Model (CAPM) — ความหมายและการใช้งานของ Beta
- Efficient Market Hypothesis (EMH) — ทำไม Warren Buffett ถึงไม่เชื่อเรื่องนี้ 100%
- Factor Investing — Fama-French Three Factor Model และ beyond
- Asset Allocation — Strategic vs. Tactical Allocation
- Rebalancing — ทำไมและทำอย่างไร
- Risk-Adjusted Return Metrics — Sharpe Ratio, Sortino Ratio, Maximum Drawdown

---

## ชั้นที่ 4 — ขั้นสูง: Advanced & Specialized Topics

### 4.1 Quantitative Finance (จุดที่ CS + Finance พบกัน)

- Stochastic Calculus เบื้องต้น — Brownian Motion และ Ito's Lemma
- Options Pricing — Black-Scholes Model และ Greeks (Delta, Gamma, Theta, Vega, Rho)
- Algorithmic Trading — Strategy Design, Signal Generation, Execution
- Statistical Arbitrage — Pairs Trading, Mean Reversion Strategies
- Machine Learning in Finance — Supervised Learning สำหรับ Price Prediction, NLP สำหรับ Sentiment Analysis
- Risk Management — Value at Risk (VaR), Expected Shortfall, Stress Testing
- High-Frequency Trading (HFT) — แนวคิดและข้อถกเถียงด้านจริยธรรม

### 4.2 Macroeconomics สำหรับนักลงทุน

- ดอกเบี้ยนโยบาย (Policy Rate) และผลกระทบต่อตลาด
- Inflation, Deflation, และ Stagflation — อ่านสัญญาณเหล่านี้อย่างไร
- Business Cycle — ตลาดหุ้นอยู่ที่จุดไหนของวัฏจักร
- Global Macro — ความสัมพันธ์ระหว่าง FX, Bond Yields และ Equity Markets
- Central Bank Policy — Fed, Bank of Thailand และผลกระทบต่อ Portfolio

### 4.3 Behavioral Finance

- Cognitive Biases ในการลงทุน — Overconfidence Bias, Anchoring, Loss Aversion
- Market Sentiment และ Crowd Psychology
- Prospect Theory (Kahneman & Tversky) — ทำไมมนุษย์ตัดสินใจทางการเงินไม่ Rational

---

## แผนการศึกษาที่ผมแนะนำสำหรับคุณโดยเฉพาะ

เนื่องจากคุณมีพื้นฐาน CS และสนใจ research ผมแนะนำให้คุณเดินสองเส้นทางพร้อมกัน คือเส้นทาง **Conceptual** (เรียนทฤษฎีและบริบท) และเส้นทาง **Applied** (ลงมือทำด้วยโค้ดและเครื่องมือจริง) ทั้งสองเส้นทางนี้จะเสริมกันตลอดเวลา เพราะทฤษฎีที่ไม่มี application คือความรู้ที่ตาย และ application ที่ไม่มีทฤษฎีคือการพนัน

---

## หนังสือและ Resources ที่ผมแนะนำ — จัดเรียงตามลำดับการอ่าน

**สำหรับรากฐาน Personal Finance:** _The Psychology of Money_ โดย Morgan Housel (2020) เป็นจุดเริ่มต้นที่ดีที่สุดในความเห็นของผม เพราะมันสอนว่าทำไมมนุษย์ถึงตัดสินใจทางการเงินผิดพลาดซ้ำๆ ก่อนที่คุณจะรู้วิธีลงทุน คุณต้องรู้วิธีคิดก่อน

_The Millionaire Next Door_ โดย Thomas J. Stanley & William D. Danko (1996) หนังสือเล่มนี้จะทำลายภาพจำที่ผิดๆ เกี่ยวกับความมั่งคั่งทิ้งไปได้เลย

**สำหรับการลงทุนพื้นฐาน:** _The Little Book of Common Sense Investing_ โดย John C. Bogle (2007) Bogle คือผู้ก่อตั้ง Vanguard และผู้สร้าง Index Fund แนวคิดในหนังสือเล่มนี้เรียบง่ายแต่ทรงพลังมาก และมีงานวิจัยรองรับอย่างแน่นหนา

_The Intelligent Investor_ โดย Benjamin Graham (1949, revised 2003) นี่คือหนังสือที่ Warren Buffett เรียกว่า "the best book about investing ever written" Graham เป็นอาจารย์ของ Buffett และหนังสือเล่มนี้สอนหลักการ Value Investing ที่ยังใช้ได้จนถึงทุกวันนี้

**สำหรับ Portfolio Theory:** _A Random Walk Down Wall Street_ โดย Burton G. Malkiel (1973, updated regularly) Malkiel โต้เถียงว่าตลาดมี Efficiency สูงมากจนแทบไม่มีนักลงทุนคนไหน Beat the Market ได้อย่างสม่ำเสมอในระยะยาว อ่านแล้วคุณจะคิดได้เองว่าตัวเองเห็นด้วยหรือไม่

**สำหรับ Quantitative Finance โดยเฉพาะ:** _Quantitative Finance for Dummies_ โดย Steve Bell (2016) อย่าปล่อยให้ชื่อหลอกคุณ หนังสือเล่มนี้ cover คณิตศาสตร์ที่จำเป็นได้ครบถ้วนและอ่านง่ายกว่า textbook มาก เหมาะสำหรับ entry point

_Python for Finance_ โดย Yves Hilpisch (2nd Edition, 2018, O'Reilly) นี่คือหนังสือที่ผมแนะนำให้คุณอย่างแรงที่สุดในฐานะ CS student Hilpisch สอน Quant Finance ผ่าน Python โดยตรง ตั้งแต่ Data Analysis ไปจนถึง Options Pricing และ Algorithmic Trading

_Options, Futures, and Other Derivatives_ โดย John C. Hull (ฉบับที่ 11, 2021) นี่คือ "Bible" ของ Derivatives ทุกคณะ Finance ระดับโลกใช้หนังสือเล่มนี้ เมื่อคุณพร้อมสำหรับ Advanced Topics นี่คือหนังสือที่ต้องมี

**สำหรับ Behavioral Finance:** _Thinking, Fast and Slow_ โดย Daniel Kahneman (2011) Kahneman คือนักจิตวิทยาที่ได้รับรางวัล Nobel ด้านเศรษฐศาสตร์ หนังสือเล่มนี้อธิบายว่าสมองมนุษย์ทำงานอย่างไร และทำไมถึง bias เสมอในสถานการณ์ที่ไม่แน่นอน ซึ่งตลาดการเงินคือสถานการณ์นั้น

**Online Courses ที่ verify แล้วว่าดี:** Coursera มี Specialization ชื่อ **"Investment Management"** จาก University of Geneva ที่ cover Portfolio Theory และ Behavioral Finance อย่างครบถ้วน และ **"Financial Engineering and Risk Management"** จาก Columbia University สำหรับ Quant track นอกจากนี้ MIT OpenCourseWare มีหลักสูตร **18.S096 Topics in Mathematics with Applications in Finance** ที่เปิดให้เรียนฟรี ซึ่ง cover Mathematics ที่ใช้ใน Quant Finance โดยตรง

**สำหรับ Tax ในประเทศไทย:** ผมแนะนำให้อ่านเอกสารโดยตรงจากเว็บไซต์ **กรมสรรพากร (rd.go.th)** และ **ตลาดหลักทรัพย์แห่งประเทศไทย (set.or.th)** เพราะกฎหมายภาษีเปลี่ยนแปลงได้ สิ่งที่เป็น print ในหนังสืออาจล้าสมัยได้

---

## ข้อความสุดท้ายจากผมในฐานะ Professor

สิ่งที่ทำให้คุณแตกต่างจากนักเรียนทั่วไปคือคุณมี background CS และคุณเริ่มเร็ว จงใช้ทั้งสองข้อนี้ให้เต็มที่ เรียนทฤษฎีแล้ว implement มันเป็นโค้ด ทดสอบด้วย Paper Trading อ่านงานวิจัย (SSRN.com มีงานวิจัยฟรีมากมาย) แล้วตั้งคำถามกับทุกสิ่งที่คุณอ่าน เพราะใน Quantitative Finance คำถามที่ดีมีค่ามากกว่าคำตอบที่รับมาโดยไม่ตรวจสอบ

คุณอยากให้ผมช่วยวางแผนการเรียนเป็น Timeline รายเดือนไหม หรืออยากให้เจาะลึกหัวข้อไหนก่อนเป็นพิเศษ?

---

_หมายเหตุ: หนังสือและ Resources ทั้งหมดที่แนะนำเป็นสิ่งพิมพ์หรือแพลตฟอร์มที่มีอยู่จริงและสามารถตรวจสอบได้ ข้อมูลเกี่ยวกับภาษีและกฎระเบียบอ้างอิงจากกรอบที่มีอยู่ในปัจจุบัน แต่ควรตรวจสอบกับแหล่งข้อมูลทางการล่าสุดเสมอ คำแนะนำนี้เป็นไปเพื่อการศึกษาเท่านั้น ไม่ใช่คำแนะนำทางการเงินโดยตรง_