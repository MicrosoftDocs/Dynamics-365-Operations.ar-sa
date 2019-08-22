---
title: الإبلاغ كمنتهي بموقع غير خاضع للتحكم بواسطة لوحة الترخيص (استمارة تقديم، أيار/مايو 2016)
description: يبين دليل المهام هذا مثالاً للإبلاغ كمنته إلى موقع غير خاضع للتحكم بواسطة لوحة الترخيص.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e87e0400ca2e9c30c0c1a642931dd8b8dec4845b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843495"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a>الإبلاغ كمنتهي بموقع غير خاضع للتحكم بواسطة لوحة الترخيص (استمارة تقديم، أيار/مايو 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

يبين دليل المهام هذا مثالاً للإبلاغ كمنته إلى موقع غير خاضع للتحكم بواسطة لوحة الترخيص. تُعد سياسة العمل القابلة للتطبيق المتطلب الأساسي لهذه المهمة. أظهر دليل المهمة السابقة إعداد سياسة العمل. يتطلب دليل المهام هذا الإصدار 7.0.1 أو أحدث من تطبيق Dynamics AX.




## <a name="set-up-an-output-location"></a>إعداد موقع المخرجات
1. انتقل إلى إدارة المؤسسة > الموارد > مجموعات الموارد.
2. في القائمة، حدد مجموعة الموارد "5102".
3. انقر فوق "تحرير".
4. في الحقل "مستودع المخرجات"، أدخل "51".
5. في الحقل "موقع الإخراج"، أدخل "001".
    * الموقع 001 غير خاضع للتحكم بواسطة لوحة الترخيص. يمكنك إعداد موقع إخراج غير لوحة غير مرخصة فقط في حالة وجود سياسة عمل قابلة للتطبيق للموقع.  

## <a name="create-a-production-order-and-report-it-as-finished"></a>إنشاء أمر الإنتاج والإبلاغ عنه كمنته
1. قم بإغلاق الصفحة.
2. انتقل إلى التحكم بالإنتاج‬ > أوامر الإنتاج > كافة أوامر الإنتاج.
3. انقر فوق "أمر إنتاج جديد".
4. في الحقل "رقم الصنف"، أدخل "L0101".
5. انقر فوق إنشاء.
6. في جزء الإجراءات، انقر فوق "أمر إنتاج".
7. انقر فوق "تقدير".
8. انقر فوق موافق.
9. انقر فوق "بدء".
10. انقر فوق علامة التبويب عام.
11. في الحقل "‏‫استهلاك قائمة مكونات الصنف التلقائي‬"، حدد "أبدًا".
12. انقر فوق موافق.
13. انقر فوق "الإبلاغ كمنتهٍ".
14. انقر فوق علامة التبويب عام.
15. حدد "نعم" في الحقل "قبول الخطأ".
16. انقر فوق موافق.
17. في جزء الإجراءات، انقر فوق "مستودع".
18. انقر فوق تفاصيل العمل.
    * عندما تم الإبلاغ عن أمر الإنتاج كمنته، فإنه لا يتم إنشاء عمل للتخزين. يحدث هذا لأنه يتم تعريف سياسة عمل تمنع إنشاء العمل عندما يتم الإبلاغ عن المنتج L0101 كمنته للموقع 001.  

