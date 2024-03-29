---
title: تكوين عمليات الاعتماد في سير عمل
description: استخدم الإجراء التالي لتكوين خصائص عملية الاعتماد.
author: ChrisGarty
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99a4e131b2afa65152d8e9d41b8405895d997250
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070792"
---
# <a name="configure-approval-processes-in-a-workflow"></a>تكوين عمليات الاعتماد في سير عمل

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

استخدم الإجراء التالي لتكوين خصائص عملية الاعتماد.

لتكوين عملية اعتماد في محرر سير العمل، انقر بزر الماوس الأيمن فوق عنصر الاعتماد، ثم انقر فوق **خصائص** لفتح النموذج **خصائص**.

## <a name="name-the-approval-process"></a>تسمية عملية الاعتماد

اتباع الخطوات التالية لإدخال اسم لعملية الاعتماد.

1. في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.
2. في حقل **الاسم**، أدخل اسمًا فريدًا لعملية الاعتماد.

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a>تحديد الوقت الذي يجب أن يقوم خلاله النظام بشكل تلقائي باتخاذ الإجراء المناسب على المستند

يمكنك تكوين النظام بحيث يتخذ الإجراء المناسب على المستند بشكل تلقائي إذا تمت تلبية شروط معينة. على سبيل المثال، باستطاعة النظام اعتماد تقارير المصروفات ذات مبالغ إجمالية أقل من 100 دولار أمريكي. اتبع هذه الخطوات لتحديد الوقت الذي يجب أن يتخذ النظام خلاله الإجراء المناسب على المستند.

1. في الجزء الأيمن، انقر فوق **إجراءات تلقائية‬**.
2. حدد خانة الاختيار **تمكين الإجراءات التلقائية**.
3. انقر فوق **إضافة شرط**.
4. يتيح إمكانية إدخال شرط.
5. أدخل شروطًا إضافية، إذا لزم الأمر.
6. للتأكد من تكوين الشروط التي قمت بإدخالها بشكل صحيح، أكمل الخطوات التالية:

    1. انقر فوق **اختبار** لفتح النموذج **اختبار حالة سير العمل**.
    2. حدد سجلاً في المنطقة **‏‏التحقق من الشرط** من النموذج.
    3. انقر فوق **اختبار**. سيقوم النظام بتقييم السجل لمعرفة ما إذا كان يستوفي الشروط التي قمت بتحديدها أم لا.
    4. انقر فوق **موافق** أو **إلغاء الأمر** للعودة إلى النموذج **خصائص**.

7. من القائمة **إجراء الإكمال التلقائي**، حدد الإجراء الذي يجب أن يتخذه النظام على المستند.

## <a name="specify-when-notifications-are-sent"></a>تحديد وقت إرسال الإخطارات

يمكن إرسال الإخطارات إلى الأشخاص عند الموافقة على مستند أو رفضه أو تفويضه أو تصعيده، أو عند طلب إجراء تغيير. اتبع هذه الخطوات لتحديد الوقت الذي يتم فيه ارسال الإخطارات، والأشخاص الذين يتم إرسال الإخطارات إليهم.

1. في الجزء الأيمن، انقر فوق **الإخطارات‬**.
2. حدد خانة الاختيار إلى جانب الأحداث التي يجب إرسال الإخطارات بشأنها:

    - **تفويض** – عند تعيين المستند إلى مستخدم آخر للاعتماد.
    - **تصعيد** – عندما لا ينفذ المستخدم أي إجراء على المستند في الوقت المخصص لذلك.
    - **موافقة** – عند الموافقة على مستند.
    - **رفض** – عند رفض مستند.
    - **طلب تغيير** – عندما يطالب المستخدم المعين بإجراء تغيير على المستند الذي تم إرساله.

3. حدد الصف المتعلق بحدث قمت بتحديده في الخطوة 2.
4. انقر فوق علامة التبويب **نص الإخطار‬**.
5. في مربع النص، أدخل نص الإخطار‬.
6. لإضفاء طابع شخصي على النص، يمكنك إدراج عناصر نائبة، يتم استبدالها بالبيانات المناسبة عند عرضها للمستخدمين. لإدراج عنصر نائب، اتبع هذه الخطوات:

    1. انقر داخل مربع النص في المكان الذي يجب أن يظهر فيه العنصر النائب.
    2. انقر فوق **إدراج عنصر نائب**.
    3. في القائمة التي تظهر، حدد العنصر النائب المراد إدراجه.
    4. انقر فوق **إدراج**.

7. لإضافة ترجمات الإخطارات، انقر فوق **ترجمات**. في النموذج الذي يظهر، اتبع الخطوات التالية:

    1. انقر فوق **إضافة**.
    2. في القائمة التي تظهر، حدد اللغة التي ستستخدمها لإدخال النص.
    3. في مربع النص **النص المترجم‬**، أدخل النص.
    4. لتخصيص النص، يمكنك إدراج عناصر نائبة.
    5. انقر فوق **إغلاق**.

8. انقر فوق علامة تبويب **المستلم**.
9. حدد الأشخاص الذين ستُرسل الإخطارات إليهم. حدد أحد الخيارات في الجدول التالي، ثم اتبع الخطوات الإضافية للخيار قبل الانتقال إلى الخطوة 10.

    <table>
    <thead>
    <tr>
    <th>الخيار</th>
    <th>مستلمو الإخطارات</th>
    <th>الخطوات الإضافية</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><strong>المشارك</strong></td>
    <td>المستخدمون الذين تم تعيينهم إلى مجموعة معينة أو دور معين</td>
    <td>
    <ol>
    <li>بعد تحديد <strong>المشارك</strong>، انقر فوق علامة التبويب <strong>مستند إلى الدور‬</strong>.</li>
    <li>في قائمة <strong>نوع المشارك</strong>، حدد نوع المجموعة أو الدور لإرسال الإخطارات إليه.</li>
    <li>في قائمة <strong>المشارك</strong>، حدد المجموعة أو الدور لإرسال الإخطارات له.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><strong>مستخدم سير العمل</strong></td>
    <td>المستخدمون المشاركون في سير العمل الحالي</td>
    <td>
    <ol>
    <li>بعد تحديد <strong>مستخدم سير العمل</strong>، انقر فوق علامة تبويب <strong>سير العمل</strong>.</li>
    <li>في قائمة <strong>مستخدم سير العمل</strong>، حدد مستخدمًا يشارك في سير العمل.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><strong>المستخدم</strong></td>
    <td>مستخدمون محددون</td>
    <td>
    <ol>
    <li>بعد تحديد <strong>المستخدم</strong>، انقر فوق علامة تبويب <strong>المستخدم</strong>.</li>
    <li>حدد المستخدمين لإرسال الإخطارات إليهم، ثم انقل هؤلاء المستخدمين إلى قائمة <strong>المستخدمون المحددون</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. كرر الخطوات من 3 إلى 9 لكل الأحداث التي قمت بتحديدها في الخطوة 2.

## <a name="specify-a-final-approver"></a> تحديد معتمد نهائي

يمكنك تعيين المعتمد النهائي للسيناريوهات حيث المعتمد هو الشخص الذي قدم المستند للموافقة عليه وحيث يجري استخدام "عدم السماح للمرسِل بالموافقة‬". اتبع الخطوات التالية لتحديد المعتمد النهائي.

1. في محرر سير العمل، انقر بزر الماوس الأيمن فوق عنصر الاعتماد، ثم حدد **خصائص** لفتح النموذج **خصائص**.
2. في الجزء الأيمن، انقر فوق **إعدادات متقدمة‬**.
3. حدد خانة الاختيار **استخدام المعتمد النهائي**.
4. من القائمة، حدد المستخدم الذي سيكون المعتمد النهائي.

## <a name="set-a-time-limit"></a>قم بتعيين حد زمني

اتبع الخطوات التالية إذا كان يجب إكمال عملية الاعتماد في وقت معين.

> [!NOTE]
> ستقوم الخيارات التي تحددها هنا بإبطال الخيارات التي حددتها في الناحيتين  **تعيين** و **تصعيد** لكل خطوة اعتماد.

1. في الجزء الأيمن، انقر فوق **إعدادات متقدمة‬**.
2. حدد خانة الاختيار **تعيين حد زمني** **لعنصر سير العمل**.
3. في حقل **المدة**، حدد الوقت الذي يجب خلاله إكمال عملية الاعتماد. وحدد أحد الخيارات التالية:

    - **ساعات** - أدخل عدد الساعات التي يجب خلالها إكمال عملية الاعتماد. ثم حدد التقويم الذي تستخدمه مؤسستك، وأدخل معلومات حول أسبوع عمل مؤسستك.
    - **أيام** - أدخل عدد الأيام التي يجب خلالها إكمال عملية الاعتماد. ثم حدد التقويم الذي تستخدمه مؤسستك، وأدخل معلومات حول أسبوع عمل مؤسستك.
    - **أسابيع** - أدخل عدد الأسابيع التي يجب خلالها إكمال عملية الاعتماد.
    - **أشهر** - حدد اليوم والأسبوع الذي يجب أن تكون فيه عملية الاعتماد مكتملة. على سبيل المثال، ربما تريد إكمال عملية الاعتماد في يوم الجمعة من الأسبوع الثالث من الشهر.
    - **سنوات** - حدد اليوم والأسبوع والشهر الذي يجب أن تكون فيه عملية الاعتماد مكتملة. على سبيل المثال، ربما تريد إكمال عملية الاعتماد في يوم الجمعة من الأسبوع الثالث من شهر ديسمبر.

4. إذا تم تجاوز الحد الزمني فسيقوم النظام باتخاذ الإجراء المناسب على المستند. من القائمة **إجراء**، حدد الإجراء الذي يجب أن يقوم النظام باتخاذه.

## <a name="specify-which-actions-are-available-to-the-user"></a>تحديد الإجراءات المتاحة للمستخدم

عند تعيين مستند إلى مستخدم للاعتماد، يجب أن يقوم المستخدم بإجراء في المستند. اتبع هذه الخطوات لتحديد الإجراءات التي يمكن للمستخدم اتخاذها على المستند الذي تم إرساله.

1. في الجزء الأيمن، انقر فوق **إعدادات متقدمة‬**.
2. حدد خانة الاختيار **موافقة** إذا كان باستطاعة المستخدم الموافقة على المستند.
3. حدد خانة الاختيار **رفض** إذا كان باستطاعة المستخدم رفض المستند.
4. حدد خانة الاختيار **طلب التغيير** لكي يتمكن المستخدم من طلب إدخال تغييرات على المستند.
5. حدد خانة الاختيار **تفويض** إذا كان باستطاعة المستخدم تعيين المستند إلى مستخدم آخر للموافقة عليه.

> [!NOTE]
> توقف العمل بخانة الاختيار **تمكين الإجراءات من قائمة العمل في مدخل الشركة على الإنترنت**‬.

## <a name="configure-the-approval-steps"></a> تكوين خطوات الاعتماد

تتكون عملية الاعتماد من خطوات اعتماد. أكمل الإجراء التالي لإضافة خطوات عملية الاعتماد وتكوين الخطوات.

1. في محرر سير العمل، انقر نقرًا مزدوجًا فوق عملية الاعتماد. يعرض محرر سير العمل خطوات عملية الاعتماد.
2. لإضافة خطوة اعتماد، اسحب الخطوة من ناحية **عناصر سير العمل** إلى لوحة الرسم.
3. لتكوين خطوة اعتماد، راجع [تكوين خطوات اعتماد في سير عمل](configure-approval-step-workflow.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]