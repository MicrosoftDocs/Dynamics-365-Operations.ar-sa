---
title: الترحيل باستخدام الدفاتر المشتقة
description: توضح هذه المقالة كيفية استخدام الدفاتر المشتقة.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b58b2da949211f7eef804af98c866bf5074d47f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187120"
---
# <a name="post-with-derived-books"></a>الترحيل باستخدام الدفاتر المشتقة

[!include [banner](../includes/banner.md)]

توضح هذه المقالة كيفية استخدام الدفاتر المشتقة.

عندما تقوم بترحيل الحركات لدفتر يحتوي على دفاتر مشتقة، يتم ترحيل حركات الدفاتر المشتقة تلقائيًا في دفاتر اليومية أو أوامر الشراء أو فواتير النص الحر. ومع ذلك، إذا قمت بإعداد حركات الدفاتر الأساسية في دفتر يومية الأصول الثابتة، فيمكنك عرض مبالغ الحركات المشتقة وتعديلها قبل ترحيلها.
-   يتم تحديث حسابات معينة، مثل ضريبة المبيعات وحسابات العميل أو المورد مرة واحدة فقط عن طريق ترحيلات الدفتر الأساسي. ويتم ترحيل حركات الدفاتر المشتقة إلى الحسابات التي تم تحديدها للدفتر المشتق في صفحة ملفات تعريف ترحيل الأصول الثابتة.‬
-   يتم استخدام الاستحواذ في أغلب الأحيان كنوع الحركة للدفاتر المشتقة. سوف تستخدم هذا عند لزوم تطبيق الدفتر والدفتر المشتق على الأصول الثابتة من وقت الاستحواذ على الأصل الثابت.
-   كما يُمكن أيضًا تطبيق قيم أخرى لنوع الحركة. على سبيل المثال، إذا كان الدفتر الأساسي والدفاتر المشتقة لهما الفترات الزمنية نفسها فيما يتعلق بعمليات البيع أو التخلص، فستتوفر كافة أنواع حركات الأصول الثابتة لإعداد دفتر مشتق.

> [!WARNING]
> سيكون مبلغ الإهلاك الذي تم ترحيله في الدفتر المشتق هو نفسه المبلغ الذي تم ترحيله للدفتر الأساسي. وإذا كانت طرق الإهلاك مختلفة بين الدفاتر، فلا يجب إنشاء حركات إهلاك باستخدام العملية المشتقة. |

## <a name="example"></a>مثال 
توضح المعلومات التالية كيفية إعداد حركات الاستحواذ باستخدام وظيفة الدفتر المشتق.

1.  إنشاء الدفاتر في صفحة الدفاتر.
    -   دفتر المحاسبة: VM 1، طبقة الترحيل الحالية
    -   الدفتر للأغراض الضريبية‬: VM 2، طبقة ترحيل الضريبة

2.  في نموذج القيمة VM 1، انقر فوق علامة تبويب "الدفاتر المشتقة". حدد نموذج القيمة VM 2 في حقل "الدفتر‬"، وحدد "الاستحواذ‬" في حقل "نوع الحركة".

يمكن عندئذٍ إرفاق الدفاتر بأصول ثابتة معينة. 

عند ترحيل امتلاك لأصل ثابت بالدفتر VM 1، لا يتم ترحيل الامتلاك في VM 1 فقط، ولكن يتم ترحيله أيضًا في الدفتر المشتق VM 2. ويتم تحديث حالة دفتري قيم الأصول الثابتة إلى "فتح".‬

> [!NOTE]                                                                                                         
> إذا لم تستخدم الدفاتر المشتقة، فيجب عليك ترحيل الاستحواذ على الأصل الثابت لكل من الدفتر VM 1 والدفتر VM 2.

لمزيد من المعلومات، راجع [‏‫الدفاتر المشتقة](derived-books.md).


