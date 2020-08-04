---
title: الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Commerce
description: يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها من Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: aa18e7446a72a907fcad70f92ea529088b6cecbd
ms.sourcegitcommit: 83c7e5ab54c1cad2e21e33769cc524cfa4213f58
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/07/2020
ms.locfileid: "3539869"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها من Dynamics 365 Commerce.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

تهدف هذه القائمة إلى مساعدتك في مراعاة ميزات الإزالة وعمليات الإهلاك للتخطيط الخاص بك. 

> [!NOTE]
> يمكن العثور على معلومات مفصلة حول الكائنات في تطبيقات Finance and Operations [التقارير المرجعية التقنية](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). يمكنك مقارنة إصدارات مختلفة من هذه التقارير لمعرفة المزيد حول الكائنات التي تم تغييرها أو التي تمت إزالتها من كل إصدار من تطبيقات Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.11 من Commerce
### <a name="data-action-hooks"></a>ربط إجراءات البيانات
|   |  |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | تم إهمال ميزه ربط إجراءات البيانات بسبب مشاكل في الأداء. |
| **هل تم الاستبدال بميزة أخرى؟**   | يستحسن استخدام [‏‫عمليات تجاوز إجراءات البيانات‬](../e-commerce-extensibility/data-action-overrides.md) لتعديل منطق تسلسل العمل في طبقة إجراء البيانات.|
| **مناطق المنتجات المتأثرة**         | إجراءات بيانات قابلية توسعة التجارة الإلكترونية |
| **خيارات النشر**              | ‏‏الكل |
| **الحالة**                         | مهمل: اعتبارًا من إصدار 10.0.11 |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>دعم Retail SDK لكل من Visual Studio‏ 2015 وmsbuild 14.0 ومكتباتRetail SDK\المرجعية والأدوات
|   |  |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | تم إهمال دعم Retail SDK لـ Visual Studio 2015 وتحديثه لدعم الإصدارات 2017 وmsbuild 15.0 وجميع المكتبات المرجعية وأدوات منشئ وكيل التجارة في المجلد RetailSDK\المراجع الذي تم نقله إلى حزم NuGet لتبسيط نموذج الامتدادات وعملية ترقية SDK.|
| **هل تم الاستبدال بميزة أخرى؟**   | يستحسن اتباع المعلومات الواردة في [ترحيل Retail SDK من Visual Studio 2015 إلى Visual Studio 2017](../dev-itpro/retail-sdk/migrate-sdk.md) لتحديث نظامك. |
| **مناطق المنتجات المتأثرة**         | امتدادات Retail SDK |
| **خيارات النشر**              | ‏‏الكل |
| **الحالة**                         | مهمل: اعتبارًا من إصدار 10.0.11 |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>امتداد خادم البيع بالتجزئة باستخدام IEdmModelExtender وCommerceController
|   |  |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | تم إهمال امتداد خادم البيع بالتجزئة باستخدام IEdmModelExtender و CommerceController لتوفير نموذج امتداد مبسط. سينطوي التنفيذ الجديد على فئة عنصر التحكم فقط دون تطبيق أي فئة IEdmModelExtender إضافية. ويؤدي ذلك أيضًا إلى تجنب التبعية مع إصدار OData معين (في حالة تحديث إصدار OData، فقد يؤدي ذلك إلى إيقاف الامتدادات.) |
| **هل تم الاستبدال بميزة أخرى؟**   |  يستحسن استخدام نموذج امتداد الفئة IController عن طريق استيراد حزمة NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts). |
| **مناطق المنتجات المتأثرة**         | امتدادات خادم البيع بالتجزئة |
| **خيارات النشر**              | ‏‏الكل |
| **الحالة**                         | مهمل: اعتبارًا من إصدار 10.0.11 |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>امتداد محطة الأجهزة باستخدام IHardwareStationController
|   |  |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | تم إهمال امتداد محطة الأجهزة باستخدام IHardwareStationController لتوفير نموذج امتداد مبسط. سينطوي التنفيذ الجديد على الفئة IController فقط دون تطبيق أي فئة إضافية ولتجنب التبعية مع مكتبات محطات الأجهزة الأساسية، يحتاج الامتداد السابق إلى الرجوع إلى مكتبات متعددة. |
| **هل تم الاستبدال بميزة أخرى؟**   | يستحسن استخدام نموذج امتداد الفئة IController عن طريق استيراد حزمة NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts). |
| **مناطق المنتجات المتأثرة**         | امتدادات محطة الأجهزة |
| **خيارات النشر**              | ‏‏الكل |
| **الحالة**                         | مهمل: اعتبارًا من إصدار 10.0.11 |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.10 من Commerce
### <a name="pos-operation-803---picking-and-receiving"></a>عملية نقطة البيع 803 - الانتقاء والاستلام
|   |  |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | جارٍ إهمال عمليات الانتقاء والاستلام نظرا لإعاده التصميم الجديد للعملية. |
| **هل تم الاستبدال بميزة أخرى؟**   | نعم. ويتم استبدالها بعمليتي POS جديدتين: العملية الداخلية (804) والعملية الخارجية (805).|
| **مناطق المنتجات المتأثرة**         | تطبيق نقطة البيع (POS) |
| **خيارات النشر**              | ‏‏الكل |
| **الحالة**                         | مهمل: بدءًا من الإصدار 10.0.10، لن تتلقي عملية الانتقاء والاستلام إيه تحديثات لميزات جديدة. سيتم اجراء إصلاحات الأخطاء الهامه فقط لهذه العملية في الإصدارات المستقبلية. ويتم تشجيع كافة العملاء علي الانتقال إلى [العمليات الداخلية](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) و [العمليات الخارجية](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)، والتي ستستمر في أن تكون جزءا من مخطط المنتج طويل الأجل. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.7 من Commerce
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>واجهات API لـ Commerce GetProductAvailabilities و GetAvailableInventoryNearby
|   |  |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | تم إنشاء واجهة API محسّنة جديدة لتحل محل واجهات برمجة التطبيقات GetProductAvailabilities و GetAvailableInventoryNearby. |
| **هل تم الاستبدال بميزة أخرى؟**   | نعم: يتم استبداله بواجهات GetEstimatedAvailabilty وGetEstimatedProductWarehouseAvailability. |
| **مناطق المنتجات المتأثرة**         | SDK لتطبيق التجارة الإلكترونية |
| **خيارات النشر**              | ‏‏الكل |
| **الحالة**                         | مهمل: بدءا من الإصدار 10.0.7 ، لن يكون هناك استثمارات هندسية لـ GetProductAvailabilities وGetAvailableInventoryNearby. يجب تحويل المؤسسات التي تستخدم واجهات برمجه التطبيقات (APIs) هذه في عمليات توزيع التجارة الإلكترونية إلى واجهات برمجة تطبيقات GetEstimatedAvailabilty وGetEstimatedProductWarehouseAvailability الجديدة وتمكين [ميزة حساب إتاحة المنتج المحسنة](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>الإعلانات السابقة حول الميزات التي تمت إزالتها أو إهمالها
لمعرفه المزيد حول الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة، راجع [‏‫الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة‬](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).
