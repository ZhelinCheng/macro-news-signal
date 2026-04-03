# 指数字段说明

## 1. 美国10年期 TIPS 债券字段说明

本文档用于说明获取自 CNBC Quote Cache 的 **美国10年期通胀保值债券 (U.S. 10 Year TIPS)** JSON 数据字段含义。

### 1. 证券基础信息 (General Information)
| 字段名 | 类型 | 说明 | 示例 |
| :--- | :--- | :--- | :--- |
| `symbol` | String | 证券交易代码 | `US10YTIP` |
| `name` | String | 证券完整名称 | `U.S. 10 Year TIPS` |
| `shortName` | String | 证券简称 | `U.S. 10 Year TIPS` |
| `type` | String | 资产大类 | `BOND` (债券) |
| `subType` | String | 资产子类 | `Government Bond` (国债) |
| `currencyCode` | String | 交易货币 | `USD` |
| `countryCode` | String | 国家代码 | `EU` (注：此处数据源标记可能为系统预设) |

### 2. 收益率行情数据 (Yield Quotes)
**注意：** 在债券行情中，`last` 字段通常代表**收益率 (Yield)**，而非价格。

| 字段名 | 类型 | 说明 | 示例 |
| :--- | :--- | :--- | :--- |
| `last` | String | **当前最新收益率** | `1.976%` |
| `previous_day_closing` | String | 前一交易日收盘收益率 | `1.956%` |
| `change` | String | 收益率绝对变动值 | `+0.02` |
| `change_pct` | String | 收益率变动百分比 | `-0.18%` |
| `changetype` | String | 变动趋势状态 | `UP` |
| `open` / `high` / `low` | String | 当日开盘/最高/最低收益率 | `0.00%` (可能暂无成交) |
| `last_timedate` | String | 最后更新时间 (美东) | `11:59 AM EDT` |

### 3. 债券价格数据 (Bond Price)
反映债券本身的交易价格（通常以面值的百分比表示）。

| 字段名 | 类型 | 说明 | 示例 |
| :--- | :--- | :--- | :--- |
| `bond_last_price` | String | **债券最新价格** | `99.1016` |
| `bond_prev_day_closing_price`| String | 债券前一交易日收盘价 | `99.2813` |
| `bond_change_price` | String | 价格绝对变动额 | `+0.18` |
| `bond_change_pct_price` | String | 价格变动百分比 | `+0.1813%` |
| `bond_changetype` | String | 价格变动趋势 | `UP` |

### 4. 债券属性与周期 (Bond Attributes)
| 字段名 | 类型 | 说明 | 示例 |
| :--- | :--- | :--- | :--- |
| `coupon` | String | **票面利率** (固定利息) | `1.875%` |
| `maturity_date` | String | **到期日期** | `2036-01-15` |
| `yrhiprice` / `yrhidate` | String | 一年内收益率最高点及日期 | `2.46` / `04/11/25` |
| `yrloprice` / `yrlodate` | String | 一年内收益率最低点及日期 | `1.60` / `04/04/25` |
| `issue_id` | String | 发行 ID (系统唯一标识) | `23200538` |

### 5. 其他系统字段
* `realTime`: 是否为实时流数据 (`true`/`false`)。
* `curmktstatus`: 当前市场状态 (`REG_MKT` 表示正常交易时段)。
* `volume`: 交易量（债券通常显示为 0 或由流动性决定）。
* `provider`: 数据提供方。


## 2. ICE 美元指数 (.DXY) 字段说明

本文档用于说明 **ICE 美元指数 (U.S. Dollar Index)** 的实时行情数据字段含义。

### 1. 基础信息 (General Information)
| 字段名 | 类型 | 说明 | 示例 |
| :--- | :--- | :--- | :--- |
| `symbol` | String | 指数交易代码 | `.DXY` |
| `name` | String | 指数全称 | `ICE U.S. Dollar Index` |
| `type` | String | 资产类型 | `INDEX` (指数) |
| `subType` | String | 子类型 | `Index` |
| `currencyCode` | String | 计价货币 | `USD` |
| `last_time` | String | 数据最后更新的 ISO 时间戳 | `2026-04-03T12:25:34...` |

##### 2. 价格行情 (Price Quotes)
| 字段名 | 类型 | 说明 | 示例 |
| :--- | :--- | :--- | :--- |
| `last` | String | **当前最新指数点位** | `100.183` |
| `open` | String | 今日开盘价 | `99.986` |
| `high` | String | 今日最高价 | `100.186` |
| `low` | String | 今日最低价 | `99.946` |
| `previous_day_closing` | String | 前一交易日收盘价 | `100.028` |

### 3. 涨跌数据 (Change Data)
| 字段名 | 类型 | 说明 | 示例 |
| :--- | :--- | :--- | :--- |
| `change` | String | 指数绝对涨跌点数 | `+0.155` |
| `change_pct` | String | 指数涨跌百分比 | `+0.15%` |
| `changetype` | String | 涨跌状态 | `UP` (上涨) |

### 4. 历史极端值 (Yearly Range)
| 字段名 | 类型 | 说明 | 示例 |
| :--- | :--- | :--- | :--- |
| `yrhiprice` | String | 过去 52 周最高点位 | `104.31` |
| `yrhidate` | String | 52 周最高点出现日期 | `04/02/25` |
| `yrloprice` | String | 过去 52 周最低点位 | `95.55` |
| `yrlodate` | String | 52 周最低点出现日期 | `01/27/26` |

### 5. 系统及状态字段 (System Status)
| 字段名 | 类型 | 说明 | 示例 |
| :--- | :--- | :--- | :--- |
| `realTime` | String | 是否为实时数据 | `true` |
| `curmktstatus` | String | 市场当前状态 | `REG_MKT` (常规交易) |
| `timeZone` | String | 数据所处时区 | `EDT` (美国东部夏令时) |
| `is_halted` | String | 是否停牌/交易中断 | `N` (否) |
| `issue_id` | String | 证券/指数唯一标识码 | `586968` |