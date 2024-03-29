---
title: إنشاء حساب تخزين Azure في مدخل Azure
description: تشرح هذه المقالة كيفية إنشاء حساب تخزين Azure للفوترة الإلكترونية.
author: gionoder
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 5eca23985c48f4e577bd4567cc2e324df5aa9690
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291625"
---
# <a name="create-an-azure-storage-account-in-the-azure-portal"></a>إنشاء حساب تخزين Azure في مدخل Azure

[!include [banner](../includes/banner.md)]

يتم تخزين جميع الملفات الإلكترونية التي يتم إنشاؤها بواسطة خدمة الفواتير الإلكترونية أو الانتقال إلى الخدمة أثناء المعالجة في حاويات حساب تخزين Microsoft Azure. للتأكد من أن الفواتير الإلكترونية يمكنها الوصول إلى تلك الحاويات، يجب عليك تقديم رمز توقيع الوصول المشترك (SAS) لحساب التخزين إلى خدمة الفوترة الإلكترونية. بالإضافة إلى ذلك، لضمان تخزين الرمز المميز بشكل آمن، لا تقدم رمز SAS مباشرة. بدلاً من ذلك، قم بتخزينه في المخزن الرئيسي في Azure، وقم بتوفير سر المخزن الرئيسي في Azure.

1. افتح حساب التخزين الذي تخطط لاستخدامه مع خدمة الفوترة الإلكترونية.
2. انتقل إلى **الإعدادات** \> **التكوين**، وتأكد من تعيين معلمة **السماح بالوصول العام إلى الكائن الثنائي كبير الحجم** إلى **ممكّن**.
3. انتقل إلى **تخزين البيانات** \> **الحاويات**، وأنشئ حاوية جديدة.
4. أدخل اسمًا للحاوية، وقم بتعيين حقل **مستوى الوصول العام** إلى **خاص (لا وصول مجهول الهوية)**.
5. افتح الحاوية، وانتقل إلى **الإعدادات** \> **سياسة الوصول**.
6. حدد **إضافة سياسة** لإضافة سياسة وصول مخزّنة.
7. قم بتعيين حقل **المعرف** كما هو مناسب.
8. في حقل **الأذونات**، حدد كل الأذونات.

    ![كافة الأذونات المحددة في الحقل الأذونات في مربع الحوار أضافه سياسة](media/e-invoicing-azure-1.png)

9. أدخل تاريخي البدء والانتهاء. يجب أن يكون تاريخ الانتهاء في المستقبل.
10. حدد **موافق** لحفظ السياسة، ثم احفظ تغييراتك إلى الحاوية.
11. انتقل إلى **الإعدادات** \> **رموز الوصول المشتركة**، وقم بتعيين قيم الحقول.
12. أدخل تاريخي البدء والانتهاء. يجب أن يكون تاريخ الانتهاء في المستقبل.
13. في حقل **الأذونات**، حدد الأذونات التالية:

    - مقروء
    - إضافة
    - إنشاء
    - كتابة
    - حذف
    - القائمة

14. حدد **إنشاء رمز SAS المميز وعنوان URL**.
15. انسخ القيمة وخزنها في حقل **عنوان URL لـ SAS للتخزين كبير الحجم‬**. سيتم استخدام هذه القيمة لاحقًا في هذا الإجراء وستتم الإشارة إليها على أنها *URI‏‎ توقيع الوصول المشترك*.
16. افتح المخزن الرئيسي الذي تخطط لاستخدامه مع الفوترة الإلكترونية.
17. انتقل إلى **الإعدادات** \> **الأسرار**، وحدد **إنشاء/استيراد** لإنشاء سر.
18. في الصفحة **إنشاء سر**، في الحقل **خيارات التحميل**، حدد **يدوي**.
19. أدخل اسم السر. سيتم استخدام هذا الاسم أثناء إعداد الخدمة في Regulatory Configuration Services (RCS)، وستتم الإشارة إليها على أنه *اسم سر المخزن الرئيسي*. لمزيد من المعلومات حول كيفية إعداد RCS، راجع [إعداد Regulatory Configuration Service (RCS)](e-invoicing-set-up-rcs.md).
20. في حقل **القيمة**، أدخل عنوان URI لتوقيع الوصول المشترك الذي نسخته مسبقًا.
21. حدد **إنشاء**.
