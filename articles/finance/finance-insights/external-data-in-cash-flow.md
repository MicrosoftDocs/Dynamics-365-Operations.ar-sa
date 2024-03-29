---
title: البيانات الخارجية في توقعات التدفق النقدي
description: تصف هذه المقالة خطوات الإعداد التي يجب إكمالها بحيث يمكن إدخال البيانات الخارجية أو استيرادها في توقعات التدفق النقدي.
author: RyanCCarlson2
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f0cb05770dc2fbd4e13af261b5f0a0e117a2f6d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846933"
---
# <a name="external-data-in-cash-flow-forecasts"></a>البيانات الخارجية في توقعات التدفق النقدي

[!include [banner](../includes/banner.md)]

يمكن إدخال البيانات الخارجية أو استيرادها إلى تقديرات تدفقات نقدية. تصف هذه المقالة خطوات الإعداد الخاصة باستخدام البيانات الخارجية التي تمكنك من تضمين البيانات الخارجية في تقدير التدفقات النقدية.

## <a name="external-data-setup"></a>إعداد البيانات الخارجية

استخدم علامة التبويب **المصدر الخارجي** في صفحة **إعداد التنبؤ بالتدفق النقدي** (**إدارة النقد والبنوك \> التنبؤ بالتدفق النقدي \> إعداد التنبؤ بالتدفق النقدي**) لإدخال الإعدادات التي تدعم استخدام البيانات الخارجية في تقديرات التدفقات النقدية.

يمكن إدخال البيانات الخارجية أو استيرادها إلى تقديرات تدفقات نقدية. قبل إدخال البيانات الخارجية أو استيرادها، يجب إعداد المصادر الخارجية. في علامة التبويب **المصدر الخارجي**، قم بإعداد فئات التدفق النقدي الخارجي. يمكن أن تكون الفئة إما **صادرة** أو **واردة**. يجب تحديد **السيولة** باعتبارها نوع الترحيل. في شبكة **إعدادات الكيان القانوني**، حدد الكيانات القانونية والحسابات الرئيسية المقابلة التي تنطبق عليها فئات التدفقات النقدية الخارجية.

لمزيد من المعلومات حول كيفية إعداد تنبؤات التدفق النقدي، راجع [التنبؤ بالتدفق النقدي](../cash-bank-management/cash-flow-forecasting.md).

## <a name="enter-external-data"></a>إدخال البيانات الخارجية

لإدخال وتعديل بيانات خارجية للتنبؤات بالتدفقات النقدية، يمكنك استخدام تجربة **الفتح في Excel**. حدد الزر **بيانات خارجية** في مساحة عمل **التنبؤ بالتدفق النقدي**، ثم حدد إما **إضافة البيانات الخارجية** أو **تحرير البيانات الخارجية الموجودة**. عند فتح الملف Microsoft Excel، فإنه يمكنك إدخال معلومات في الحقول التالية:

- **معرف الإدخال** (فريد)
- **الوصف** (اختياري)
- **اسم المصدر الخارجي** – حدد إحدى القيم في القائمة التي قمت بتحديدها عند إعداد Finance Insights.
- **كيان قانوني**
- **التاريخ**
- **المبلغ بعملة الحركة**
- **كود العملة**
- **البعد الافتراضي** (اختياري)
- **رقم المستند** (اختياري)
- **رقم الحساب** (اختياري)
- **اسم الحساب** (اختياري)

## <a name="importing-external-data-by-using-the-data-management-framework"></a>استيراد بيانات خارجية باستخدام إطار عمل إدارة البيانات

يمكنك استيراد البيانات الخارجية لتقديرات التدفقات النقدية باستخدام مساحة عمل **إدارة البيانات** والكيان المسمى **إدخال مصدر خارجي لتقدير التدفقات النقدية**.

بالإضافة إلى ذلك، إذا كان من الضروري نقل بيانات الإعداد من بيئة إلى أخرى، تصبح منطقة الكيانات التالية متاحة لجداول الإعداد المطلوبة:

- إعداد المصدر الخارجي للتنبؤ بالتدفق النقدي
- إعداد الكيان القانوني للمصدر الخارجي للتنبؤ بالتدفق النقدي

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
