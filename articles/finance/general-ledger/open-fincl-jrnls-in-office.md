---
title: فتح قوالب دفتر اليومية المالي في Office
description: يوضح هذا الموضوع المشكلات التي قد تحدث عند إنشاء دفاتر يومية مالية مخصصة باستخدام قالب Microsoft Excel.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0773f47551b2460ec310b92b67c634b433147749
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/24/2021
ms.locfileid: "6089447"
---
# <a name="open-financial-journal-templates-in-office"></a><span data-ttu-id="59e78-103">فتح قوالب دفتر اليومية المالي في Office</span><span class="sxs-lookup"><span data-stu-id="59e78-103">Open financial journal templates in Office</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59e78-104">يوضح هذا الموضوع المشكلات التي قد تحدث عند إنشاء دفاتر يومية مالية مخصصة باستخدام قالب Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="59e78-104">This topic describes issues that might occur when you create custom financial journals by using a Microsoft Excel template.</span></span>

## <a name="symptom"></a><span data-ttu-id="59e78-105">العَرَضْ</span><span class="sxs-lookup"><span data-stu-id="59e78-105">Symptom</span></span>

<span data-ttu-id="59e78-106">لقد قمت بإنشاء قالب Excel مخصص لدفاتر اليومية المالية، ولكنه لا يظهر في قائمة **فتح السطور في Excel**.</span><span class="sxs-lookup"><span data-stu-id="59e78-106">You created a custom Excel template for financial journals, but it doesn't appear on the **Open lines in Excel** menu.</span></span> <span data-ttu-id="59e78-107">وبدلاً من ذلك، يظهر القالب في القائمة، ويتم فتح قالب مختلف ولكن عند تحديده.</span><span class="sxs-lookup"><span data-stu-id="59e78-107">Alternatively, it does appear on the menu, a different template is opened but when you select it.</span></span>

## <a name="resolution"></a><span data-ttu-id="59e78-108">الحل</span><span class="sxs-lookup"><span data-stu-id="59e78-108">Resolution</span></span>

<span data-ttu-id="59e78-109">تستخدم وظيفة "فتح في Excel" الافتراضية مصدر البيانات الجذر (الجدول) للصفحة الحالية لتحديد قوالب Office أو كيانات البيانات التي تظهر في صورة خيارات في قائمة **فتح في Excel**.</span><span class="sxs-lookup"><span data-stu-id="59e78-109">The default Open in Excel functionality uses the root data source (table) of the current page to determine which Office templates or data entities appear as options on the **Open in Excel** menu.</span></span> <span data-ttu-id="59e78-110">لا يعد هذا السلوك تجربة مثالية لدفاتر اليومية المالية، نظرًا لأن دفاتر اليومية المالية تستخدم نفس الجداول (LedgerJournalTable وLedgerJournalTrans) باعتبارها مصدر البيانات الجذر للعديد من الأنواع الأخرى لدفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="59e78-110">This behavior isn't an ideal experience for financial journals, because financial journals use the same tables (LedgerJournalTable and LedgerJournalTrans) as the root data source of many other types of journals.</span></span>

<span data-ttu-id="59e78-111">بالنسبة لدفاتر اليومية المالية، يتمثل الهدف من وظيفة "فتح السطور في Excel" في عرض القوالب التي تم تصميمها لدفتر اليومية الذي تعمل فيه حاليًا في سياق، مثل دفتر اليومية العام أو دفتر يومية المدفوعات.</span><span class="sxs-lookup"><span data-stu-id="59e78-111">For financial journals, the Open Lines in Excel functionality is intended to show templates that are designed for the journal that you're currently working in the context of, such as the general journal or a payment journal.</span></span> <span data-ttu-id="59e78-112">على سبيل المثال، سيتم تصميم قالب مخصص يتم استخدامه مع دفتر يومية مدفوعات المورد لفرض حسابك الأساسي في صورة حساب مورد.</span><span class="sxs-lookup"><span data-stu-id="59e78-112">For example, a template that is intended to be used with a vendor payment journal will be designed to enforce your primary account as a vendor account.</span></span>

<span data-ttu-id="59e78-113">إذا كنت ترغب في ترقية قالب حتى يصبح متوفرًا على قائمتي **فتح السطور في Excel‬** و **فتح في Excel**، فإن تجربة المطور السهلة تتمثل في تنفيذ واجهة **LedgerIJournalExcelTemplate** وتوسيع الدرجة **DocuTemplateRegistrationBase**.</span><span class="sxs-lookup"><span data-stu-id="59e78-113">If you want to promote a template so that it's available on the **Open lines in Excel** and **Open in Excel** menus, an easy developer experience is to implement the **LedgerIJournalExcelTemplate** interface and extend the **DocuTemplateRegistrationBase** class.</span></span> <span data-ttu-id="59e78-114">يتم تطبيق العديد من أمثلة هذا النهج في النظام.</span><span class="sxs-lookup"><span data-stu-id="59e78-114">Many examples of this approach are implemented in the system.</span></span> <span data-ttu-id="59e78-115">يتمثل أحد الأمثلة التي يمكن استخدامها على سبيل المرجعية في واجهة **LedgerDailyJournalExcelTemplate** التي تم إنشاؤها لدفتر اليومية العام (أو دفتر اليومية اليومي).</span><span class="sxs-lookup"><span data-stu-id="59e78-115">One example that can be used for reference is the **LedgerDailyJournalExcelTemplate** interface that was created for the general journal (or daily journal).</span></span>

<span data-ttu-id="59e78-116">عند تنفيذ واجهة **LedgerIJournalExcelTemplate** لقالبك، ستقوم قائمة **فتح السطور في Excel** بتصفية القوالب حسب نوع دفتر اليومية الخاص بك، وستعرض القوالب المتاحة لدفتر اليومية هذا فقط.</span><span class="sxs-lookup"><span data-stu-id="59e78-116">When the **LedgerIJournalExcelTemplate** interface is implemented for your template, the **Open Lines in Excel** menu will filter templates by the journal type of your journal and will show only the templates that are available for that journal.</span></span> <span data-ttu-id="59e78-117">توفر الواجهة أيضًا طريقة تحقق من الصحة تضمن عدم إمكانية فتح قالب لدفتر يومية في حالة عدم تحقيقه لمتطلبات نوع الحساب.</span><span class="sxs-lookup"><span data-stu-id="59e78-117">The interface also provides a validation method that ensures that a template can't be opened for a journal if it doesn't meet the account type requirements.</span></span> <span data-ttu-id="59e78-118">على سبيل المثال، يمكنك تحديد وجوب أن يكون الحساب من نوع **المورد** أو **دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="59e78-118">For example, you can specify that the account type must be of the **Vendor** or **Ledger** type.</span></span>

<span data-ttu-id="59e78-119">لمزيد من المعلومات حول هذه الوظيفة، راجع [إضافة قوالب إلى قائمة "فتح السطور في Excel"](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span><span class="sxs-lookup"><span data-stu-id="59e78-119">For more information about this functionality, see [Add templates to the Open lines in Excel menu](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span></span>
