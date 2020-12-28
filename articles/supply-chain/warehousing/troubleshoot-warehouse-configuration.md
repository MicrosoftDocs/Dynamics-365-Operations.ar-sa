---
title: استكشاف أخطاء تكوين المستودع وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء تكوين Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9bbe92627f53b3b4b04597be144d602b3cae7ed7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646097"
---
# <a name="troubleshoot-warehouse-configuration"></a>استكشاف أخطاء تكوين المستودع وإصلاحها

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء تكوين Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a>أتلقى رسالة الخطا التالية: "لوحه الترخيص أو الموقع غير صحيح."

### <a name="issue-description"></a>وصف المشكلة

تظهر رسالة الخطا هذه عند مسح معرف لوحه الترخيص أو الموقع.

### <a name="issue-resolution"></a>حل المشكلة

تاكد من ان معرف لوح الترخيص غير محجوز بواسطة شيء آخر. وتستخدم هذه المشكلة لتحدث عندما يكون أحد المستخدمين الذي قام بفحصه في تطبيق المستودع هو موقع صالح ومعرف لوحه ترخيص صالح. ومع ذلك ، تم حل هذه المشكلة في الإصدار 10.0.11.

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a>أتلقى رسالة الخطا التالية: "يجب تحديد لوحه الترخيص لهذا الموقع."

### <a name="issue-description"></a>وصف المشكلة

تظهر رسالة الخطا هذه إذا قمت بإنشاء أمر تحويل باستخدام مستودع ممكن لأداره المستودعات المتقدمة (WMS) ، ثم بعد اكتمال العمل ، فانك تحاول تاكيد الشحن.

### <a name="issue-resolution"></a>حل المشكلة

حقل **موقع الاستلام الافتراضي** فارغ لمخزن بضاعة بالطريق للمستودع "من". لحل هذه المشكلة ، حدد موقع استلام افتراضي في مخزن البضاعة بالطريق. تاكد من ان هذا الموقع هو لوحه الترخيص – التي يتم التحكم بها.

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a>أتلقى رسالة الخطا التالية: "لا يمكنك إنشاء بند قالب عمل لتغيير حاله المخزون لان نوع العمل غير صالح. حدد نوع عمل مختلف."

### <a name="issue-description"></a>وصف المشكلة

بالنسبة لقالب عمل، لا يمكنك تحديد *تغيير حاله المخزون* في العمود **نوع العمل** الخاص بقسم **تفاصيل قالب العمل**.

### <a name="issue-resolution"></a>حل المشكلة

يتم هذا السلوك بسبب التصميم. يتم استخدام نوع العمل *تغيير حاله المخزون* فقط من قبل عمليات النظام. لا يمكن تكوينها. ونظرا لان قائمه أنواع العمل قد تم إصلاحها علي انها قائمه تعداد ، لا يمكن تصفيه الإدخالات الاضافيه خارج القائمة المنسدلة **نوع العمل**.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>أتلقى رسالة الخطا التالية: "الكمية غير صالحة للوحدة 1%."

### <a name="issue-description"></a>وصف المشكلة

الكمية غير صالحه لوحده *ea* عند وجود عمل انتقاء يحتوي علي لوحات ترخيص متعددة في موقع واحد.

### <a name="issue-resolution"></a>حل المشكلة

تحقق من تعيين الحقلين **معرف مجموعه تسلسل الوحدات** و **تحويلات الوحدات** في متغير المنتج أو المنتج الذي تم إصداره بشكل صحيح.

لاحظ انه تم تحسين رسالة الخطا في 10.0.15 الإصدار (راجع [قاعدة المعارف 4581627 ](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). رسالة الخطا الجديدة هي ، "الكمية غير صالحه. المتوقع %1 %2."

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>في موجات الموقع التي يضع فيها عمل التوريد ، لا يقوم خيار المضاعفة SKU بتقييم الإجراءات الموجهة متعددة المواقع.

### <a name="issue-description"></a>وصف المشكلة

لا يقوم موجه المواقع الخاصة بنوع أمر عمل *أوامر المبيعات* ونوع العمل *تخزين* بتقييم الإجراءات الموجهة متعددة المواقع عند تحديد الخيار **SKU متعددة**. يتم تقييم الاجراء الخاص بالتوجيه في الموقع الأول فقط.

### <a name="issue-resolution"></a>حل المشكلة

تمت أضافه ميزه جديده، *تقييم كافة الإجراءات لتوجيهات المواقع SKU المتعددة*، في الإصدار 10.0.15 (راجع [قاعدة المعارف 4579866 ](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). هذه الميزة تقيم كافة الإجراءات لموجهات مواقع SKU متعددة. إذا تطلبت هذه الميزة ، فاستخدم [أداره الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتشغيلها.

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a>لا يمكنني استخدام تطبيق المستودع لاجراء انتقاء جزئي.

### <a name="issue-description"></a>وصف المشكلة

بالنسبة لأوامر التوريد والتحويل ، لا يمكنك تخطي الأصناف واجراء انتقاء جزئي.

### <a name="issue-resolution"></a>حل المشكلة

في الصفحة **عناصر قائمه الجهاز المحمول**، لكل عنصر قائمه تم اعداده لمعالجه أوامر المبيعات أو أوامر التحويل، قم بتعيين خيار **السماح بتقسيم العمل** في علامة التبويب السريعة **عام** إلى *نعم*.

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a>كيف يمكنني اجراء تغيير في حاله المخزون للعمل الجزئي للكمية؟

### <a name="issue-description"></a>وصف المشكلة

الرغبة في القيام بتغيير في حاله المخزون لكميه جزئيه من المجموعة.

### <a name="issue-resolution"></a>حل المشكلة

لتمكين العاملين من اجراء هذا التغيير ، يمكنك إنشاء عنصر قائمه لتطبيق المستودع. في صفحة **عناصر قائمة الجهاز المحمول**، أنشئ عناصر قائمة لأحد الطرق التالية:

- **الوضع:** *العمل*
- **استخدام العمل الموجود:** *لا*
- **عملية إنشاء العمل:** *الحركة*
- **عرض حالة المخزون:** *نعم*

يمكنك تعيين حقول أخرى في الصفحة كما هو مطلوب.
