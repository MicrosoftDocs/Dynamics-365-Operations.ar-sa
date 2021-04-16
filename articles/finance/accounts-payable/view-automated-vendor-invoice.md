---
title: عرض نتائج أتمتة فاتورة المورد (معاينة)
description: يوضح هذا الموضوع كيفيه عرض حاله فواتير المورد الموجودة في عمليه الإرسال إلى سير العمل التلقائية.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 872ec404da0cce41c4ea0f882a3fa8af56316ce3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837215"
---
# <a name="view-vendor-invoice-automation-results"></a><span data-ttu-id="583ed-103">عرض نتائج التنفيذ التلقائي لفاتورة المورد</span><span class="sxs-lookup"><span data-stu-id="583ed-103">View vendor invoice automation results</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="583ed-104">يوضح هذا الموضوع كيفيه عرض حاله فواتير المورد الموجودة في عمليه الإرسال إلى سير العمل التلقائية.</span><span class="sxs-lookup"><span data-stu-id="583ed-104">This topic explains how to view the status of vendor invoices that are in the automated submit-to-workflow process.</span></span> <span data-ttu-id="583ed-105">ويتم الاحتفاظ بتفاصيل محفوظات الأتمتة لكل فاتورة مورد مستورده.</span><span class="sxs-lookup"><span data-stu-id="583ed-105">Details of the automation history are maintained for each imported vendor invoice.</span></span> <span data-ttu-id="583ed-106">وفقا للعمليات التجارية التي قمت بتنفيذها تلقائيا، تعرض صفحه **فواتير المورد المعلقة** قيمتي **حاله مطابقه الإيصال التلقائية** و **حالة الإرسال التلقائي إلى سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="583ed-106">Depending on the business processes that you've automated, the **Pending vendor invoices** page shows **Automated receipt match status** and **Automated submit to workflow status** values.</span></span> <span data-ttu-id="583ed-107">يمكنك عرض التفاصيل وتقديم خطه للتركيز علي الفواتير التي فشلت في تنفيذ خطوه تلقائية.</span><span class="sxs-lookup"><span data-stu-id="583ed-107">You can view the details and make a plan to focus on the invoices that failed an automated step.</span></span> <span data-ttu-id="583ed-108">وبعد ذلك ، بعد تصحيح المشكلة، يمكنك استئناف العملية التلقائية للفاتورة التي تم استيرادها.</span><span class="sxs-lookup"><span data-stu-id="583ed-108">Then, after you correct the issue, you can resume the automated process for the imported invoice.</span></span>

<span data-ttu-id="583ed-109">قبل ان تتمكن من تحرير فاتورة تم تسليمها، يجب إيقاف المعالجة التلقائية مؤقتا.</span><span class="sxs-lookup"><span data-stu-id="583ed-109">Before you can edit an invoice that has been submitted, you must pause the automated processing.</span></span> <span data-ttu-id="583ed-110">إذا كان يجب إيقاف فاتورة في عمليه الإرسال إلى سير العمل تلقائيا، قم بتعيين **حقل تضمين في المعالجة التلقائية** إلى **لا** في الصفحة **فواتير الموردين**.</span><span class="sxs-lookup"><span data-stu-id="583ed-110">If an invoice in the automated submit-to-workflow process must be paused, set the **Include in Automated processing** field to **No** on the **Vendor invoices** page.</span></span> <span data-ttu-id="583ed-111">وبعد ذلك لن يتم تشغيل الأتمتة حتى يتم تعيين **التضمين في المعالجة التلقائية** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="583ed-111">Automation then won't run until **Include in Automated processing** is set to **Yes**.</span></span> <span data-ttu-id="583ed-112">يمكن إيقاف الفاتورة مؤقتا من الأتمتة إذا لم تكن في نظام سير العمل كما انها لا تستخدم من قبل العملية التلقائية.</span><span class="sxs-lookup"><span data-stu-id="583ed-112">An invoice can be paused from further automation if it isn't yet in the workflow system and isn't used by the automated process.</span></span>

<span data-ttu-id="583ed-113">إذا كانت الفاتورة المستوردة خاضعه لعمليه الإرسال إلى سير العمل، فيمكنك عرض قيمه **حاله الأتمتة** في الصفحة **فواتير المورد**.</span><span class="sxs-lookup"><span data-stu-id="583ed-113">If an imported invoice is subject to the submit-to-workflow process, you can view its **Automation status** value on the **Vendor invoices** page.</span></span> <span data-ttu-id="583ed-114">يتم تعقب الحالات التالية:</span><span class="sxs-lookup"><span data-stu-id="583ed-114">The following statuses are tracked:</span></span>

- <span data-ttu-id="583ed-115">**مضمن** – يتم تشغيل العمليات التلقائية التي تم تحديدها في الصفحة **محددات الحسابات الدائنة** بشكل صحيح ولكن لم يتم إكمالها بعد.</span><span class="sxs-lookup"><span data-stu-id="583ed-115">**Included** – The automated processes that are defined on the **Accounts payable parameters** page are running correctly but haven't yet been completed.</span></span>
- <span data-ttu-id="583ed-116">**متوقف مؤقتا** – تم تشغيل العمليات التلقائية التي تم تحديدها في الصفحة **معلمات الحسابات الدائنة**، ولكن توجد خطوه واحده علي الأقل في العملية.</span><span class="sxs-lookup"><span data-stu-id="583ed-116">**Paused** – The automated processes that are defined on the **Accounts payable parameters** page have run, but at least one step in the process failed.</span></span> <span data-ttu-id="583ed-117">يتم تطبيق الحالة **تم الإيقاف المؤقت** أيضا إذا تم تعيين الحقل **تضمين في المعالجة التلقائية** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="583ed-117">The **Paused** status is also applied if the **Include in automated processing** field is set to **No**.</span></span> <span data-ttu-id="583ed-118">يمكنك عرض حالات الفشل عن طريق تحديد **عرض أحدث النتائج**.</span><span class="sxs-lookup"><span data-stu-id="583ed-118">You can view the failures by selecting **View most recent results**.</span></span>
- <span data-ttu-id="583ed-119">**في سير العمل** – تم إرسال الفاتورة المستوردة إلى نظام سير العمل، سواء كانت بواسطة عمليه الإرسال إلى سير العمل التلقائية أو يدويا.</span><span class="sxs-lookup"><span data-stu-id="583ed-119">**In workflow** – The imported invoice has been submitted to the workflow system, either by the automated submit-to-workflow process or manually.</span></span>
- <span data-ttu-id="583ed-120">**إكمال سير العمل** – تم إكمال عمليه سير العمل للفاتورة التي تم استيرادها.</span><span class="sxs-lookup"><span data-stu-id="583ed-120">**Workflow complete** – The workflow process has been completed for the imported invoice.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]