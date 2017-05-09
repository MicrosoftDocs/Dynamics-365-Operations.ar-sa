---
title: "بحث التنقل"
description: "تشرح هذه المقالة كيفية استخدام وظيفة البحث للانتقال إلى الصفحات في Microsoft Dynamics 365 for Operations."
author: aneesmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 87fed576f8cf358520d94f5cd5b326ff9801913a
ms.lasthandoff: 03/31/2017


---

# <a name="navigation-search"></a>بحث التنقل

[!include[banner](../includes/banner.md)]


تشرح هذه المقالة كيفية استخدام وظيفة البحث للانتقال إلى الصفحات في Microsoft Dynamics 365 for Operations.

يوفر Dynamics 365 for Operations وظائف لمجموعة واسعة من القطاعات والصناعات. يحتوي هذا التطبيق على عدد من النواحي والصفحات لمساعدتك في تنفيذ المهام المختلفة. للبحث بسرعة عن الصفحات التي تحتاجها لإكمال المهام الخاصة بك، استخدم ميزة بحث التنقل.‬ ولاستخدام هذه الميزة، انقر فوق رمز **البحث** لعرض مربع **البحث**. ويمكنك بعد ذلك كتابة كلمة واحدة أو أكثر في المربع. ويقوم النظام بالبحث على الفور عن الصفحات ذات الصلة في التطبيق التي تتطابق مع الكلمات التي أدخلتها. على سبيل المثال، يمكنك كتابة "فاتورة المورد" كإدخال، ثم يعرض النظام النتائج المطابقة لهذا الإدخال. **ملاحظة:** يساعدك مربع **البحث** في البحث عن والتنقل إلى الصفحات. لن يساعدك في البحث عن بيانات أو إجراءات محددة. 

[![مربع بحث](./media/search-box.png)](./media/search-box.png) تقوم ميزة بحث التنقل أيضًا بدور طريقة رائعة للتنقل بسرعة إلى صفحة معينة. على سبيل المثال، إذا كنت موظف حسابات دائنة يستخدم كثيرًا صفحة **دفتر يومية المدفوعات**‬‏‫، يمكنك إدخال "دفتر يومية المدفوعات" في مربع البحث. ونظراً لأن الإدخال مطابق تمامًا لعنوان الصفحة، فإنه يتم سرد الصفحة في أعلى نتائج البحث، ويمكن التنقل بسرعة إليها.‬ 

[![البحث عن دفتر يومية المدفوعات](./media/searching-for-payment-journal.png)](./media/searching-for-payment-journal.png) 

تعرض قائمة نتائج البحث عنوان الصفحة فضلاً عن مسار التنقل. ويساعدك هذا في إدراك موقع الصفحة في التطبيق. كما يساعدك على التفريق بين اثنين أو أكثر من الصفحات المتشابهة في النتائج. وعند البحث عن صفحة، تتم مطابقة الإدخال مع عنوان الصفحة، بالإضافة إلى مسار التنقل الخاص بها. على سبيل المثال، إذا قمت بإدخال "المدينة" في مربع البحث** **، فستشاهد نتائج الصفحات المتوفرة لك في منطقة "الحسابات المدينة" على الرغم من أن عناوين الصفحات لا تتضمن كلمة "المدينة". 

[![البحث عن كلمة المدينة](./media/search-for-the-word-receivable.png)](./media/search-for-the-word-receivable.png) 

من منظور الأمن والإدارة، تُظهر وظيفة بحث التنقل فقط:

-   الصفحات التي تم تمكينها في التكوين الحالي (عبر مفاتيح التكوين).
-   الصفحات التي يصل إليها المستخدم استناداً إلى دور المستخدم

تقتصر قائمة نتائج البحث على 10 أصناف. إذا لم تجد ما تبحث عنه في النتائج، يجب أن تحاول تحسين أو تحديث الإدخال. ومن منظور التطوير، من السهل جدًا الاستفادة من وظيفة بحث التنقل نظرًا لأنه لا يوجد أي تأخير بين نشر أصناف القائمة وقدرتها على الظهور في نتائج البحث. وطالما أن أصناف القائمة يتم الارتباط بها من جزء التنقل أو لوحة المعلومات، فسوف تصبح قابلة للبحث فيها تلقائياً. كما تتضمن وظيفة بحث التنقل ميزة مطلوبة كثيرًا لمستخدمي الطاقة: القدرة على التنقل بسرعة إلى صفحة استناداً إلى اسم النموذج التقني. ويعتاد العديد من المستخدمين كثيرًا على ذلك النظام لأنهم يعرفون أسماء النماذج الدقيقة التي يتعاملون معها. وإذا كنت أحد المستخدمين، فإنه يمكنك إدخال **النموذج:** متبوعاً باسم النموذج الذي تبحث عنه. على سبيل المثال، إذا قمت بإدخال **النموذج: فاتورة المورد**، فسوف تُظهر نتائج البحث كافة الصفحات التي يبدأ فيها اسم النموذج بـ **فاتورة المورد**. 

[![البحث عن نموذج فاتورة المورد](./media/search-for-form-vendinvoice.png)](./media/search-for-form-vendinvoice.png)



