# 当前学习计划

## 90 天目标

以独立完成一个包含 REST API、参数校验、异常处理和数据库访问的 Spring Boot 项目为主线。主要知识点建立地图，但只有通过作品、运行结果、解释和迁移验证的内容才计为掌握。

## 第 1 个 7 天周期（2026-09-08 至 2026-09-14）

周期成果：完成一个可运行的命令行订单小程序，包含商品对象、订单金额计算、订单状态与非法输入处理。

- Day 1：方法契约、参数、局部变量与返回值。
- Day 2：类、对象、构造器与封装。
- Day 3：String、枚举和日期。
- Day 4：List、泛型与集合计算。
- Day 5：异常处理并组装命令行订单小程序。
- Day 6：15～30 分钟无提示复测，或休息。
- Day 7：休息，或补齐未通过任务。

### Day 1 详细安排（60 分钟）

- 唯一核心目标：准确说明并实现方法参数、局部变量和返回值的数据流。
- 5 分钟：无提示回忆字段、参数和返回值。
- 10 分钟：方法签名与返回值类型的最少讲解。
- 25 分钟：完成订单价格计算的核心方法。
- 10 分钟：编译、阅读错误信息并修复。
- 5 分钟：更换业务规则做迁移。
- 5 分钟：反向讲解与记录证据。
- 完成标准：边界样本运行正确；能说明每个变量的来源和返回值代表什么；迁移题通过。
- 提交证据：运行输出、解释、最高提示等级和作品相对路径。

### Day 1 完成记录（2026-09-09）

- 订单实付金额三个样本输出 `120 / 198 / 0`，一次编译通过。
- 库存迁移三个样本输出 `68 / 35 / 7`，业务语义与返回类型正确。
- `int` 的返回类型含义经一次纠正后理解；加入 2026-09-12 延迟复测。
- 下一步：Day 2 类、对象、构造器与封装；开始前复测字段、参数与 `this`。

### Day 2 完成记录（2026-09-10）

- `OrderItem` 构造器一次编译通过，输出 `键盘 / 199 / 2 / 398`。
- `StockItem.sell` 在公开方法中校验并修改私有库存，输出 `10 / 7 / 5` 后按预期抛出异常。
- 能说明封装通过统一入口校验来防止对象进入非法状态。
- 字段、同名参数与 `this` 的到期复测未通过；一次失败不降级，顺延至 2026-09-13 再测。
- 下一步：Day 3 String、枚举与日期；开始前复测 List 增强 for。

### Day 3 完成记录（2026-09-14）

- 到期的增强 `for` 复测未独立通过；展示固定语法后输出 `键盘 / 鼠标 / 显示器`，顺延复测。
- `Order` 使用 `String`、`OrderStatus` 与 `LocalDate` 后运行输出 `ORD-20260911-001 / PAID / 2026-09-11`。
- 迁移到 `MemberAccount` 与 `Delivery`；经提示后能区分构造器与 `main`，最终输出会员与物流样例。
- `enum` 与 `LocalDate` 在首次迁移前讲解不足，相关初始错误不计入学习者证据。
- `Delivery` 中字段与参数的数据来源再次对应错误；修正后运行通过，顺延至 2026-09-17 无提示复测。
- 下一步：Day 4 `List`、泛型与集合统计；开始前完成返回类型复测。

### Day 4 完成记录（2026-09-14）

- 返回类型延迟复测的退款业务结果独立正确，漏分号由教练机械修复，输出 `180 / 45`。
- `CartCalculator` 与 `WarehouseCalculator` 的增强 `for` 结构正确，最终分别输出 `562 / 0` 与 `243 / 0`。
- 金额汇总曾连续保留示例中的 `count + 1`；展示正确累加模型后完成。
- 库存迁移中连续直接访问 `private` 字段；展示后改为调用 `public calculateStockValue()`。
- 学习者主动指出多文件调用路径不透明；以后每个多文件任务先提供“入口 → 调用 → 返回”地图与方法定位规则。
- 下一步：Day 5 异常处理并组装命令行订单程序；2026-09-19 复测集合汇总和公开方法调用。

## 第 2 个 7 天周期（2026-09-15 至 2026-09-21）

周期成果：补齐第 1 周未完成部分，将商品、订单状态、集合统计与异常处理组装成可运行的命令行订单程序。

从 2026-09-15 起，每个学习日调整为 90 分钟：10 分钟复测、20 分钟最少必要讲解、40 分钟核心实战、15 分钟迁移与调试、5 分钟复盘记录。

- 学习日 1：返回类型短复测；`List<String>`、`List<Order>` 与增强 `for`。
- 学习日 2：集合金额统计与边界样本。
- 学习日 3：异常处理与非法订单输入。
- 学习日 4：组装命令行订单程序。
- 学习日 5：无提示复测、修复和小型重构。
- 其余两天：休息或补齐未通过任务。

## 大纲处理

- 保留：L1 核心基础。
- 提前穿插：L2 类与对象、L3 集合框架。
- 已纳入：Maven 工程、依赖管理、测试与生命周期。
- 暂缓：Stream、并发、Spring 与数据访问；L1 工程基础复测通过后逐步纳入。

## 调整历史

- 2026-09-08：根据诊断将起点定为 L1；原因是条件、对象和集合均需提示或示范。构造器与集合提前穿插，以支撑首周订单作品。复测条件为无提示完成变量角色解释和 List 遍历。
- 2026-09-10：字段与参数延迟复测未通过，但构造器编码和封装迁移通过；整体 Level 保持 L1，不重复整天内容。将该复测顺延至 2026-09-13，Day 3 按原计划继续。
- 2026-09-14：第 1 周实际完成 3 个学习日，未压缩剩余内容。建立第 2 周滚动计划，先补齐逾期复测，再继续集合、异常和命令行作品；整体 Level 保持 L1。
- 2026-09-14：多文件阅读障碍被确认后，后续练习固定增加调用路径文档；该支架只帮助定位文件，不替代学习者实现核心业务逻辑。
- 2026-09-15：根据学习者明确要求，将每日学习时间从 60 分钟调整为 90 分钟；增加的时间优先用于跨文件调用追踪、迁移和调试，不扩张当天唯一核心行为。
- 2026-09-16：学习者主动将练习迁移到 Maven 标准项目目录 `src/main/java`，为各学习日加入 package，并把调用地图集中到 `docs`；后续编译验证改用 `mvn test`，不再逐文件运行 `javac`。

### Day 5 完成记录（2026-09-16）

- `Day5Runner` 正确捕获非法订单数量，输出两次成功和一次失败，并继续处理后续订单。
- `PaymentRunner` 将异常处理迁移到支付金额与余额不足场景；对象类型经一次纠正，方法业务含义经一次纠正后输出四个正确样例。
- 最终 `OrderConsoleApp` 在多文件调用链中正确接收 `OrderReceipt`，输出 `473 / 非法数量异常 / 249`。
- 学习者将全体练习迁移到 Maven 标准项目结构并加入 package；`mvn test` 通过，项目级运行 `day5.OrderConsoleApp` 通过。
- 下一步：2026-09-17 先复测增强 for 与构造器，再学习 Maven/package 结构和基础测试。

### Day 6 完成记录（2026-09-16）

- `PackageRunner` 正确使用 `package day6.app` 和 `import day6.catalog.Product`，跨包创建商品并输出名称与价格。
- `SameNameRunner` 只导入 `day6.order.Message`，同时用全限定类名创建 `day6.payment.Message`；Maven 编译通过并分别输出订单消息、支付消息。
- 两条结果最初因 `print` 连在一起，属于展示格式，由教练机械改为 `println`；package/import 核心逻辑无错误。
- package/import 达到独立完成并通过即时迁移，安排 2026-09-21 无提示复测；整体 Level 保持 L1。
- 下一步：2026-09-17 先复测增强 for 与构造器，再学习 Maven 测试目录和第一个 JUnit 测试。

### Day 7 完成记录（2026-09-17）

- 在 Maven 项目中配置 JUnit 5 与 Surefire，理解 `src/main/java`、`src/test/java` 和 `mvn test` 的执行关系。
- `DeliveryFeeCalculatorTest` 从普通样本扩展到 `98 / 99` 规则边界；`StockServiceTest` 完成业务迁移，并用 `assertThrows` 验证异常类型和消息。
- `assertThrows`、`.class` 和 Lambda 延迟执行首次出现时讲解不完整，补充讲解后代码与运行结果正确；该困惑不计为学习者错误。
- 构造器与增强 `for` 到期复测无提示通过：字段保存正确，库存数量 `8 + 5 + 2 = 15`，空集合为 `0`。
- 最终 `mvn test` 执行 9 个测试，Failures 0、Errors 0；JUnit 安排 2026-09-22 延迟复测。
- 本课程按 90 分钟内容块设计，实际活跃学习时长未计时，不记录为已学满 90 分钟。
- 下一步：2026-09-18 复测 `String / enum / LocalDate`，再学习 Maven 依赖坐标与 `test` scope。

### Day 8 完成记录（2026-09-20）

- 类型选择延迟复测无提示通过：文本、有限状态和日期分别使用 `String`、`DeliveryStatus`、`LocalDate`。
- 集合金额汇总与公开方法边界延迟复测无提示通过：`SalesSummary` 调用 `item.calculateSubtotal()`，样例合计 `381`，空集合为 `0`。
- `PurchaseProcessor` 第一次绕过 `PurchaseService.createReceipt` 直接创建结果对象；经一次调用位置提示后，正确完成“创建请求 → 调用 service → 接收结果 → 返回文本”，异常分支也通过。
- 完整学习 Maven 依赖坐标、版本属性 `${...}`、默认 `compile` 与 `test` scope；Commons Lang 的版本最终由属性统一管理。
- scope 对照实验中，普通 `mvn test` 曾因旧的 `target/classes` 误显成功；`mvn clean test` 正确暴露生产代码无法使用 test 依赖。恢复默认 scope 后，最终 17 个测试全部通过，依赖树显示 Commons Lang 为 compile、JUnit 为 test。
- Maven 初次练习前的讲解顺序再次不符合“先讲再练”；教练暂停任务、完整重讲后再继续。此问题不计入学习者错误，后续新语法必须先完成概念、用途、完整示例与常见误区讲解。
- 本课程按 90 分钟内容块设计，实际活跃学习时长未计时，不记录为已学满 90 分钟。
- 下一步：2026-09-21 复测 package/import，再继续 Maven 生命周期与项目打包；2026-09-25 复测 scope 选择和多文件 service 调用链。

## 调整补充（2026-09-20）

- 新知识教学固定顺序：先说明为什么需要、整体位置、完整语法、每个关键标签或关键字、可运行示例和常见错误；学习者确认理解后才进入 TODO 练习。
- `mvn test` 通过不再单独视为依赖配置正确；涉及依赖作用域或编译路径时，必须执行 `mvn clean test` 并检查依赖树。

## 第 3 个 7 天周期（2026-10-12 至 2026-10-18）

周期成果：恢复三周学习间隔后的关键复测，稳定 JUnit、Maven 依赖范围和多文件对象调用链，并能独立完成测试与 JAR 打包。

- 学习日 1：package/import 延迟复测；Maven 生命周期与普通 JAR 打包。
- 学习日 2：JUnit 普通结果、边界和异常的延迟复测。
- 学习日 3：Maven 版本属性与 `compile/test` scope 延迟复测。
- 学习日 4：请求对象 → service → 结果对象调用链复测。
- 学习日 5：组合测试、依赖和打包，完成一次无提示 Maven 构建。
- 其余两天：休息或补齐未通过任务。

### Day 9 完成记录（2026-10-12）

- 不同包同名 `Notice` 的选择正确：只 import 一个类，另一个使用全限定类名；该项延迟复测通过。
- 全限定类名创建对象时漏写 `new`，并在调用两个 `getText()` 后丢弃结果、返回空字符串；展示正确表达式后修正，相关测试通过。
- 完整学习 Maven `clean / compile / test / package` 的阶段关系、`target` 目录、普通 JAR 内容和 `java -cp` 运行方式。
- 完成对照实验：`mvn clean test` 后没有 JAR，`mvn package` 后生成 `target/dixin-java-1.0-SNAPSHOT.jar`；JAR 内包含目标 class，并输出 `Maven package success`。
- 最终 Maven 构建运行 19 个测试，Failures 0、Errors 0、BUILD SUCCESS。
- `jar tf` 命令曾因反斜杠和未闭合引号进入 `pipe quote>`，退出后改用无引号命令完成；属于终端机械问题。
- 三周学习间隔只导致逾期复习重新排期，不作为降级依据；建立新的 7 天滚动周期。
- 下一步：2026-10-13 无提示完成 JUnit 普通结果、边界和异常测试复测。

### Day 10 完成记录（2026-10-13）

- 优惠券 JUnit 延迟复测首次把执行语句直接写在类体中，并出现变量名不一致、断言漏分号；展示测试方法结构后完成三个测试。
- 异常测试首次使用合法边界 `80, 80`，且只验证异常类型、遗漏消息；修正为 `50, 51` 并验证异常消息后通过。
- 迁移到提现手续费业务后，无提示独立完成普通值 `120 → 5`、精确边界 `500 → 0`、异常输入 `0` 的类型与消息验证。
- 最终 `mvn clean test` 执行 25 个测试，Failures 0、Errors 0、BUILD SUCCESS。
- JUnit 当前结论为“提示后会做并可即时迁移”，因原始延迟复测未独立通过，安排 2026-10-17 再次短复测，不重复整天内容。
- 下一步：2026-10-14 无提示复测 Maven 版本属性与 `compile/test` scope。

### Day 11 完成记录（2026-10-14）

- Commons Collections 最终使用 `${commons-collections4.version}` 统一版本，并以默认 `compile` 范围供生产代码使用。
- 版本属性首次误写成通用 `<version>`；scope 对照实验首次把 `<scope>test</scope>` 放入 `<properties>`，因此只产生未使用的普通属性。讲解 POM 父节点后完成修正与恢复。
- `mvn clean test` 编译 65 个生产源文件和 12 个测试源文件，执行 27 个测试全部通过；依赖树显示 JUnit 为 `test`、Commons Collections 为 `compile`。
- Maven 版本属性与 scope 当前为“提示下会做并可即时验证”，尚未达到延迟稳定掌握；安排 2026-10-18 短复测。
- 下一步：2026-10-15 无提示复测“请求对象 → service → 结果对象”调用链。

### Day 11 补充迁移（2026-10-14）

- 为补足当天 90 分钟内容块，将相同核心能力迁移到 Commons Codec；生产代码通过 `DigestUtils` 生成订单编号 SHA-256。
- 版本属性结构与默认 `compile` scope 判断正确；首次把 `1.17.1` 写为 `1.7.1`，并将 `groupId` `commons-codec` 套写为 `org.apache.commons`，经错误定位提示后修正。
- 理解 `groupId` 表示组织或项目家族、`artifactId` 表示具体模块；Maven 坐标与 Java package 不能互相推断。
- 最终 `mvn clean test` 执行 29 个测试全部通过；依赖树显示 JUnit 为 `test`，Lang3、Collections4、Codec 为 `compile`。
- scope 判断出现独立迁移证据，但完整坐标仍需提示；2026-10-18 复测时同时检查版本属性、坐标和 scope。

### Day 12 完成记录（2026-10-15）

- 完成物流业务的“普通参数 → `ShippingRequest` → `ShippingService` → `ShippingResult` → 字符串返回值”调用链。
- 首次把正确文本写入 `System.out.print`，但方法仍 `return ""`；讲清控制台输出和方法返回值是两条不同的数据去向后修正。
- 迁移到退款业务后，独立创建 `RefundRequest` 与 `RefundService`，调用 `createRefund` 接收 `RefundResult`，并拼接两个 getter 的返回值。
- 物流与退款共 4 个目标测试全部通过；IntelliJ 的 Maven classpath 未刷新时，使用 Maven 命令确认依赖和测试本身正常，再通过重新加载 Maven 项目修复编辑器运行。
- 当前结论为“提示下会做并可即时迁移”；调用链迁移已通过，但返回值契约因首次复测仍需完整答案提示，安排 2026-10-16 再测。
- 本课程按 90 分钟内容块设计，实际活跃学习时长未计时，不记录为已学满 90 分钟。
- 下一步：2026-10-16 无提示复测跨包对象创建与 getter 返回值，再完成第 3 周组合构建。

### Day 13 完成记录（2026-10-16）

- `ReferenceSummary` 延迟复测无提示完成：用 import 后的短类名创建订单 `Reference`，用全限定类名创建支付 `Reference`，并直接返回两个 getter 的组合值。
- 理解包名参与类的完整身份；同名类在源码、编译结果和 JAR 中都通过不同包路径区分，`import` 只是短类名书写便利。
- 迁移到库存与销售两个同名 `Record` 类后，对象创建、类型选择、int getter 与 return 流向均独立正确；首次固定文本漏写一个 `=`，属于机械格式错误，定位期望值与实际值后修正。
- `mvn clean package` 编译 80 个生产源文件和 17 个测试源文件，执行 37 个测试全部通过，并生成普通 JAR。
- JAR 中同时存在 `day13/transfer/inventory/Record.class` 与 `day13/transfer/sales/Record.class`，验证两个同名类可以依靠完整包名共存。
- 对象创建和返回值从“提示下会做并可即时迁移”提升为“独立完成并通过即时迁移”；整体 Level 保持 L1，下一项复测转向 JUnit。
- 本课程按 90 分钟内容块设计，实际活跃学习时长未计时，不记录为已学满 90 分钟。
- 下一步：2026-10-17 无提示编写普通、边界和异常 JUnit 测试，并运行 `mvn clean test`。

## 第 4 个 7 天周期（2026-10-19 至 2026-10-25）

周期成果：完成逾期关键复测，建立“接口 + 构造器”的手动依赖注入模型，并正式进入 Spring Boot，完成第一个带 GET、请求参数和 POST DTO 的分层 API。

每天以 90 分钟为基础学习块，不再作为上限；允许延长，但仍坚持“先讲再练”和每天一个可验收的核心成果。

- 2026-10-19：JUnit 普通结果、精确边界和异常断言延迟复测与迁移（已完成）。
- 2026-10-20：合并 Maven 依赖配置与生命周期。核心成果是独立完成“版本属性与完整坐标 → scope → `clean test` → `package` → 依赖树与 JAR 检查”的完整构建链。
- 2026-10-21：合并 Java 接口与构造器组装。核心成果是定义 service 接口、编写实现类，并通过构造器把接口注入调用方，形成 Spring 依赖注入前的手动模型。
- 2026-10-22：Spring Boot 第一个独立项目。学习 Spring Boot Maven 结构、启动类与 `@SpringBootApplication`，完成应用启动和上下文测试。
- 2026-10-23：第一个分层 GET API。学习 `@RestController`、`@GetMapping`，完成“HTTP 请求 → Controller → Service → 返回值”的调用链。
- 2026-10-24：GET 参数与输入边界。学习 `@PathVariable`、`@RequestParam` 与参数校验入口；开始前完成 JUnit 精确边界短复测。
- 2026-10-25：POST API 与 DTO。学习 `@PostMapping`、`@RequestBody` 和请求/响应 DTO，完成一个内存版订单创建接口；原休息日安排废弃，改为新增知识学习日。

### Day 14 完成记录（2026-10-19）

- `ParkingFeeCalculatorTest` 延迟复测中独立完成普通值 `4 → 20`、精确边界 `2 → 10`、非法值 `0` 的异常类型与消息验证。
- 迁移到 `StorageFeeCalculatorTest` 后，JUnit 方法结构、普通结果和异常断言均独立正确；最初用 `4` 与 `10` 两个普通样本，测试虽全绿但遗漏规则切换点 `7`。
- 经一次“测试通过不等于需求覆盖”的定位提示后，补齐精确边界 `7 → 14`，并保留 `10 → 23` 与 `0` 异常测试。
- 最终 `mvn clean test` 编译 82 个生产源文件和 19 个测试源文件，执行 43 个测试，Failures 0、Errors 0、BUILD SUCCESS。
- JUnit 结构与异常断言提升为独立完成并迁移；边界语法会写，但从业务规则主动推导精确边界仍需 2026-10-24 短复测。
- 三天学习间隔只顺延逾期复测，不压缩或堆叠多个核心主题；本课程按 90 分钟内容块设计，实际活跃学习时长未计时。
- 下一步：2026-10-20 无提示复测 Maven 版本属性、完整依赖坐标、POM 父节点和 scope，并使用 `mvn clean test` 与依赖树验证。

## 调整补充（2026-10-20）

- 学习者要求扩大每日内容量，并允许学习时间超过原定 90 分钟；90 分钟调整为基础学习块而非上限。
- 原 10 月 20 日 Maven 依赖配置与 10 月 21 日 Maven 生命周期合并到 10 月 20 日，以一条完整构建链验收。
- 原 10 月 22 日接口与 10 月 23 日构造器组装合并到 10 月 21 日，以“手动依赖注入”这一核心成果验收。
- 原 10 月 25 日休息或补齐安排废弃，新增 Spring Boot POST API 与 DTO。
- 合并只适用于强关联内容；如果当天核心验收未通过，未完成部分顺延，不以延长时间为由记录为掌握。

### Day 15 完成记录（2026-10-20）

- 为 Commons Text 正确声明 `commons-text.version=1.12.0`，并在同一个 dependency 中配置 `org.apache.commons:commons-text`；未写 test scope，依赖树显示 `1.12.0:compile`。
- 依次完成 `mvn clean test`、依赖树检查、`mvn package` 和 `jar tf`；明确 test 不生成 JAR，package 会经过编译和测试后生成 JAR。
- 理解普通 JAR 只包含项目生产类，不包含测试类和第三方依赖；为后续理解 Spring Boot 可执行 JAR 的 `BOOT-INF/lib` 建立对照。
- 即时迁移到 Commons Math：在未给完整 XML 的情况下，独立写出版本属性和 `org.apache.commons:commons-math3:3.6.1` 生产依赖，使用 `mvn clean package` 一次完成完整构建。
- 独立把依赖树命令改写为 Commons Math 坐标，结果显示 `3.6.1:compile`；JAR 同时包含 `ShipmentLabelFormatter.class` 与 `OrderAmountStatistics.class`。
- 最终编译 84 个生产源文件和 21 个测试源文件，执行 45 个测试，Failures 0、Errors 0；Maven POM 父节点、完整坐标、scope 和生命周期达到“延迟复测通过并可即时迁移”。
- 编辑器旧缓冲区曾覆盖教练新加的 TODO 注释，经磁盘时间证据确认后重新补回；该工具状态问题不计为学习者错误。
- 下一步：2026-10-21 学习接口、实现类和构造器组装，完成 Spring 依赖注入前的手动依赖模型。

### Day 16 完成记录（2026-10-27）

- 学习接口只声明契约、实现类通过 `implements` 与 `@Override` 提供行为，以及调用方通过构造器接收接口类型依赖。
- 完成物流计费的标准与包邮实现；同一个 `ShippingQuoteService` 替换策略后分别返回 `12` 与 `0`。
- 迁移到消息通知场景，完成 `MessageSender`、邮件/短信实现与 `NotificationService`；三组 Day 16 测试全部通过。
- 迁移题首次调用 `send` 后未把结果 `return` 给上层，编译提示“缺少返回语句”；理解返回值流向后自行修复，安排下一次在新 service 中自然复查。
- 最初接口方法体错误发生在讲解顺序不足之后，不计入学习者错误；补充完整讲解后接口声明正确。
- 原定 JUnit 精确边界与 Maven 新依赖复测已到期，进入下一周期前置短复测。
- 下一步：开启新周期前先展示并确认新的 7 天计划，确认后再进入 Spring Boot。

## 第 5 个 7 天周期（Day 17 至 Day 23，2026-10-27 确认）

周期成果：把手动“接口 + 构造器注入”连接到 Spring 容器，完成一个可启动、可测试并包含 GET、参数和 POST DTO 的分层 Spring Boot API。

- Day 17：Spring Boot 项目结构、启动类、`@SpringBootApplication` 与应用启动。
- Day 18：Spring 容器、`@Service`、组件扫描和构造器自动注入。
- Day 19：`@RestController`、`@GetMapping` 与 Controller → Service 调用链。
- Day 20：`@PathVariable`、`@RequestParam` 与输入边界；穿插 JUnit 精确边界复测。
- Day 21：`@PostMapping`、`@RequestBody`、请求 DTO 与响应 DTO。
- Day 22：休息或只补齐本周期未通过内容。
- Day 23：组合验证与周期复盘；运行测试、启动服务、请求 API，并完成 Maven 依赖和打包短复测。

每天以 90 分钟为基础学习块，可延长；继续执行“先讲再练”，所有演示、测试与目录由教练创建，学习者只完成当天唯一核心行为。

### Day 17 完成记录（2026-10-30）

- 检查真实项目 `mkt-user` 的继承链，确认有效环境为 Java 8、`yq-parent` 和 Spring Boot `2.2.4.RELEASE`；按用户要求，学习项目与该版本保持一致。
- 创建独立项目 `spring-boot-order-api`，保留既有 Java 基础项目不变；讲解启动类、Spring 容器、内置 Tomcat、starter、配置文件与 Maven 插件的职责。
- 学习者正确启用 `@SpringBootApplication` 与 `SpringApplication.run`；Java 8 下应用上下文测试通过。
- `mvn spring-boot:run` 成功启动 8081；根路径返回 404，能够作为“Tomcat 已接收请求但尚无 Controller”的证据。
- `mvn clean package` 生成约 17MB 的可执行 JAR；验证 `BOOT-INF/classes`、`BOOT-INF/lib`、`JarLauncher` 与 `Start-Class`。
- 使用 Java 8 执行 `java -jar` 再次成功启动；进程命令、端口监听与 HTTP 404 均已现场验证。
- 首次 JAR 启动命令因教练把临时 `JAVA_HOME` 赋值和变量展开写在同一命令而解析为 `/bin/java`，属于教练命令错误，不计入学习者证据。
- 下一步：Day 18 学习 Spring Bean、`@Service`、组件扫描与构造器自动注入，把 Day 16 的手动组装连接到 Spring 容器。

### Day 18 完成记录（2026-10-30）

- 从 Day 16 手动 `new` 和构造器传参切入，理解 Bean 是由 Spring 创建、保存和管理的普通 Java 对象。
- 学习 `@Service`、启动类根包向下的组件扫描，以及单构造器无需额外 `@Autowired` 的自动注入模型。
- 在订单编号场景中，正确为实现类与业务类添加 `@Service`；学习者超出单步要求，主动完成构造器字段赋值和接口返回值转交。
- 即时迁移到支付流水号场景，无纠错完成两个 Bean、接口类型构造器注入和 `PAY-2001` 返回链路。
- Spring Boot 项目共 5 个测试全部通过，Failures 0、Errors 0；测试成功证明业务对象来自容器而非手动 `new`。
- Day 16 曾出现的“调用方法但未 return”在订单和支付两个 Spring service 中连续正确，返回值流向自然复查通过。
- 下一步：Day 19 学习 `@RestController`、`@GetMapping`，完成 HTTP → Controller → Service → 实现类的 GET 调用链。
