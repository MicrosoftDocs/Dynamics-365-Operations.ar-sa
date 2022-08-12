---
title: استكشاف أخطاء اعداد Store Commerce ومشكلات التثبيت وإصلاحها
description: تشرح هذه المقالة كيفية استكشاف مشكلات الإعداد والتثبيت وإصلاحها في ملف في تطبيق Store Commerce Microsoft Dynamics 365 Commerce.
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 8af2c476ced05fc159a53131f8b51ad914a6c7c3
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/16/2022
ms.locfileid: "9168937"
---
# <a name="troubleshoot-store-commerce-setup-and-installation-issues"></a>استكشاف أخطاء اعداد Store Commerce ومشكلات التثبيت وإصلاحها

[!include [banner](../includes/banner.md)]

تشرح هذه المقالة كيفية استكشاف مشكلات الإعداد والتثبيت وإصلاحها في ملف في تطبيق Store Commerce Microsoft Dynamics 365 Commerce.

## <a name="i-cant-activate-the-app-and-i-receive-a-connectivity-error-message"></a>تعذر تنشيط التطبيق وظهور رسالة الخطا الخاصة بالاتصال

بعد ان تقوم بإدخال محدد موقع المعلومات (CPOS) لنقطه السحابة الصالحة ، قد تتلقي رسالة خطا في الاتصال مشابهه للمثال التالي:

> حدث خطا في الاتصال ، ويتعذر علي جهازك الاتصال بCPOS. قد يكون لعنوان URL الخاص ب CPOS بعض المشكلات.

في هذه الحالة ، قم بمراجعه عنوان الربط للأخطاء المطبعية ، أو حدد ما إذا كان لا يمكن الوصول إلى CPOS لأنه غير متصل.

بالاضافة إلى ذلك ، تحقق من أن إصدار Cloud Scale Unit (CSU) (9.35.\*.\*)أو الأحدث. يجب توفر CPOS أو إصدار أحدث لاستخدام تطبيق Store Commerce.

## <a name="i-cant-install-the-app-because-modern-pos-is-already-installed"></a>لا يمكنني تثبيت التطبيق لأنه تم بالفعل تثبيت النقطة الحديثة

أثناء التثبيت، قد تتلقى رسالة خطأ مثل المثال التالي:

> تم تثبيت إصدار (9.\* .\* .\*) من هذا المنتج (POS الحديثة) مسبقا من خلال المثبت القديم.

لإصلاح الخطا ، يجب إلغاء تثبيت تطبيق نقطه البيع الحديثة (مبوس) لكافة المستخدمين الموجودين علي الجهاز ثم المحاولة مره أخرى. يمكنك تاكيد ما إذا كان قد تم أزاله مبوس لكافة المستخدمين عن طريق تشغيل الأمر PowerShell التالي.

```PowerShell
Get-AppxPackage | Where-Object {$_.PackageFullName -like "Microsoft.Dynamics.*.Pos"} | Remove-AppxPackage -Allusers
```

## <a name="i-cant-activate-the-app-because-of-an-invalid-url-or-an-error-state"></a>تعذر تنشيط التطبيق بسبب وجود URL غير صالح أو حاله خطا

إذا كان عنوان الربط الخاص ب CPOS الذي قمت بإدخاله غير صالح وتريد تغييره ، أو إذا كان تطبيق Store Commerce في حاله خطا اثناء التنشيط ، فيمكنك أعاده تشغيل العملية عن طريق أعاده تعيين التطبيق. سيقوم تطبيق Store Commerce بحفظ محدد موقع معلومات CPOS صالح.

لأعاده تعيين تطبيق Store Commerce ، اتبع الخطوات التالية.

1. في القائمة أبدا **ل Windows** ، حدد واضغط (أو انقر بزر الماوس الأيمن) علي التطبيق ، ثم حدد **المزيد من \>إعدادات** التطبيق.
2. قم بالتمرير لأسفل صفحه إعدادات التطبيق حتى تعثر علي **زر أعاده التعيين** .
3. حدد **إعادة التعيين**. بعد ذلك ، عندما يُطلب منك، أكد أنك تريد إعادة تعيين التطبيق.
