---
title: استكشاف المشاكل من ترقيات تطبيقات Finance and Operations
description: يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها الذي يمكن أن يساعدك في إصلاح المشكلات ذات الصلة بترقيات تطبيقات Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a11ce426d7f30b6b124bd2022514a0201c2b332c
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131211"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>استكشاف المشاكل من ترقيات تطبيقات Finance and Operations

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وDataverse. على وجه التحديد، يوفر هذا الموضوع المعلومات التي يمكن أن تساعدك في إصلاح المشكلات ذات الصلة بترقيات تطبيقات Finance and Operations.

> [!IMPORTANT]
> قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD). يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.

## <a name="database-synchronization-errors"></a>أخطاء مزامنة قواعد البيانات

**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام

قد تظهر رسالة خطأ مشابهة للمثال التالي عند محاولة استخدام جدول **DualWriteProjectConfiguration** لتحديث تطبيق Finance and Operations إلى تحديث النظام الأساسي 30.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

لإصلاح المشكلة، اتبع هذه الخطوات.

1. سجل الدخول إلى الجهاز الظاهري (VM) لتطبيق Finance and Operations.
2. افتح Visual Studio كمسؤول، ثم افتح شجره مكونات البرنامج (AOT).
3. ابحث عن **DualWriteProjectConfiguration**.
4. في شجرة مكونات المنتج، انقر بزر الماوس الأيمن فوق **DualWriteProjectConfiguration**، ثم حدد **إضافة إلى مشروع جديد**. حدد **موافق** لإنشاء المشروع الجديد الذي يستخدم الخيارات الافتراضية.
5. في مستكشف الحلول، انقر بزر الماوس الأيمن فوق **خصائص المشروع**، وقم بتعيين **مزامنة قاعدة البيانات عند الإنشاء** إلى **True**.
6. قم ببناء المشروع وتأكد من نجاح البنية.
7. في قائمة **Dynamics 365**، حدد **مزامنة قاعدة البيانات**.
8. حدد **مزامنة** لإجراء مزامنة كاملة لقاعدة البيانات.
9. بعد نجاح مزامنة قاعده البيانات بالكامل، أعد تشغيل خطوة مزامنة قاعده البيانات في Microsoft Dynamics Lifecycle Services ‏(LCS) واستخدم البرامج النصية الخاصة بالترقية اليدوية حسب الحاجة، حتى يمكنك الاستمرار في عمليه التحديث.

## <a name="missing-table-columns-issue-on-maps"></a>إصدار أعمده الجدول المفقودة في التعيينات

**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام

في صفحة **الكتابة الثنائية**، قد تتلقي رسالة خطأ مشابهة للمثال التالي:

*حقل المصدر المفقود \<field name\> في المخطط.*

![مثال لرسالة الخطأ عمود المصدر مفقود](media/error_missing_field.png)

لإصلاح هذه المشكلة، اتبع أولاً الخطوات التالية للتأكد من وجود الأعمدة في الجدول.

1. سجل الدخول إلى الجهاز الظاهري لتطبيق Finance and Operations.
2. انتقل إلى **مساحات العمل \> إدارة البيانات**، حدد تجانب **معلمات إطارات العمل**، ثم في علامة التبويب **إعدادات الجدول**، حدد **تحديث قائمة الجداول** لتحديث الجداول.
3. انتقل إلى **مساحات العمل \> إدارة البيانات**، وحدد علامة التبويب **جداول البيانات**، ثم تأكد من إدارج الجدول. إذا لم يكن الجدول مدرجًا، فقم بتسجيل الدخول إلى الجهاز الظاهري لتطبيق Finance and Operations، وتأكد من توفر الجدول.
4. افتح صفحة **تعيين الجدول** من صفحة **الكتابة الثنائية** في تطبيق Finance and Operations.
5. حدد **تحديث قائمة الجداول** لملء الأعمدة تلقائيًا في تعيينات الجداول.

في حالة استمرار إصلاح المشكلة، اتبع الخطوات التالية.

> [!IMPORTANT]
> ترشدك هذه الخطوات خلال عملية حذف أحد الجداول ثم إضافته مرة أخرى. لتجنب المشكلات، تأكد من اتباع الخطوات بدقة.

1. في تطبيق Finance and Operations، انتقل إلى **مساحات العمل\> إدارة البيانات**، ثم حدد تجانب **جداول البيانات**.
2. ابحث عن الجدول الذي يفتقد إلى السمة. انقر فوق **تعديل تعيين هدف** في شريط الأدوات.
3. في الجزء **تعيين التشغيل المرحلي إلى الهدف**، انقر فوق **إنشاء تعيين للمصدر**.
4. افتح صفحة **تعيين الجدول** من صفحة **الكتابة الثنائية** في تطبيق Finance and Operations.
5. إذا كان لا يتم ملء السمة تلقائيًا في التعيين، فقم بإضافتها يدويا بالنقر فوق زر **إضافة سمة** ثم النقر فوق **حفظ**. 
6. حدد التعيين ثم انقر فوق **تشغيل**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]