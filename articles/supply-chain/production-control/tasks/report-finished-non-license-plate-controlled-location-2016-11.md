---
title: الإبلاغ كمنتهي بموقع غير خاضع للتحكم بواسطة لوحة الترخيص (استمارة تقديم، أيار/مايو 2016)
description: يبين دليل المهام هذا مثالاً للإبلاغ كمنته إلى موقع غير خاضع للتحكم بواسطة لوحة الترخيص.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f891b2e3b20993a08138dfac1aed4f4bab33c6b1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576702"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a>الإبلاغ كمنتهي بموقع غير خاضع للتحكم بواسطة لوحة الترخيص (استمارة تقديم، أيار/مايو 2016)

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]