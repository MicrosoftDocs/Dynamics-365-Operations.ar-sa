---
title: استكشاف المشكلات من ترقيات تطبيقات التمويل والعمليات
description: توفر هذه المقالة معلومات استكشاف الأخطاء وإصلاحها التي يمكنها أن تساعدك على إصلاح المشكلات ذات الصلة بترقيات تطبيقات التمويل والعمليات.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 7ab75c3a7b6c53982a32658f376a9fd148c023e4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289533"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>استكشاف المشكلات من ترقيات تطبيقات التمويل والعمليات

[!include [banner](../../includes/banner.md)]





توفر هذه المقالة معلومات استكشاف الأخطاء وإصلاحها في تكامل الكتابة المزدوجة بين تطبيقات التمويل والعمليات وDataverse. على وجه التحديد، يوفر هذا الموضوع المعلومات التي يمكن أن تساعدك في إصلاح المشكلات ذات الصلة بترقيات تطبيقات التمويل والعمليات.

> [!IMPORTANT]
> قد تتطلب بعض المشكلات التي تتناولها هذه المقالة إما منصب مسؤول النظام أو بيانات اعتماد مسؤول مستأجر Microsoft Azure Active Directory (Azure AD). يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.

## <a name="database-synchronization-errors"></a>أخطاء مزامنة قواعد البيانات

**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام

قد تظهر رسالة خطأ مشابهة للمثال التالي عند محاولة استخدام جدول **DualWriteProjectConfiguration** لتحديث تطبيق التمويل والعمليات إلى تحديث النظام الأساسي 30.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

لإصلاح المشكلة، اتبع هذه الخطوات.

1. سجل دخولك إلى الجهاز الظاهري (VM) لتطبيق التمويل والعمليات.
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

![مثال لرسالة الخطأ عمود المصدر مفقود.](media/error_missing_field.png)

لإصلاح هذه المشكلة، اتبع أولاً الخطوات التالية للتأكد من وجود الأعمدة في الجدول.

1. سجل دخولك إلى الجهاز الظاهري (VM) لتطبيق التمويل والعمليات.
2. انتقل إلى **مساحات العمل \> إدارة البيانات**، حدد تجانب **معلمات إطارات العمل**، ثم في علامة التبويب **إعدادات الجدول**، حدد **تحديث قائمة الجداول** لتحديث الجداول.
3. انتقل إلى **مساحات العمل \> إدارة البيانات**، وحدد علامة التبويب **جداول البيانات**، ثم تأكد من إدارج الجدول. إذا لم يكن الجدول مدرجًا، فقم بتسجيل الدخول إلى الجهاز الظاهري لتطبيق التمويل والعمليات، وتأكد من توفر الجدول.
4. افتح صفحة **تعيين الجدول** من صفحة **الكتابة المزدوجة** في تطبيق التمويل والعمليات.
5. حدد **تحديث قائمة الجداول** لملء الأعمدة تلقائيًا في تعيينات الجداول.

في حالة استمرار إصلاح المشكلة، اتبع الخطوات التالية.

> [!IMPORTANT]
> ترشدك هذه الخطوات خلال عملية حذف أحد الجداول ثم إضافته مرة أخرى. لتجنب المشكلات، تأكد من اتباع الخطوات بدقة.

1. في تطبيق التمويل والعمليات، انتقل إلى **مساحات العمل \> إدارة البيانات**، وحدد الإطار المتجانب **جداول البيانات**.
2. ابحث عن الجدول الذي يفتقد إلى السمة. انقر فوق **تعديل تعيين هدف** في شريط الأدوات.
3. في الجزء **تعيين التشغيل المرحلي إلى الهدف**، انقر فوق **إنشاء تعيين للمصدر**.
4. افتح صفحة **تعيين الجدول** من صفحة **الكتابة المزدوجة** في تطبيق التمويل والعمليات.
5. إذا كان لا يتم ملء السمة تلقائيًا في التعيين، فقم بإضافتها يدويا بالنقر فوق زر **إضافة سمة** ثم النقر فوق **حفظ**. 
6. حدد التعيين ثم انقر فوق **تشغيل**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
