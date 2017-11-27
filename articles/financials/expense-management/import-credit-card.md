---
title: "استيراد حركات بطاقات الائتمان وصيانتها"
description: "يشرح هذا الموضوع كيفية استيراد حركات بطاقات الائتمان ذات الصلة بالمصروفات وصيانتها. يمكن إعداد هذه الحركات بحيث يتم استيرادها تلقائيًا على جدول متكرر، أو يمكن استيرادها يدويًا كما تقتضي الحاجة."
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e640c9e44add5599be4a2e381b4ffd81f212889c
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="8aaee-104">استيراد حركات بطاقات الائتمان وصيانتها</span><span class="sxs-lookup"><span data-stu-id="8aaee-104">Import and maintain credit card transactions</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8aaee-105">يمكن إعداد حركات بطاقات الائتمان ذات الصلة بالمصروفات بحيث يتم استيرادها تلقائيًا على جدول متكرر.</span><span class="sxs-lookup"><span data-stu-id="8aaee-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="8aaee-106">أو، يمكن استيراد الحركات يدويًا حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="8aaee-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="8aaee-107">يتم استيراد حركات بطاقات الائتمان عبر كيان بيانات حركات بطاقة الائتمان.</span><span class="sxs-lookup"><span data-stu-id="8aaee-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="8aaee-108">لمزيد من المعلومات حول كيانات البيانات، راجع [كيانات البيانات](../../dev-itpro/data-entities/data-entities.md).</span><span class="sxs-lookup"><span data-stu-id="8aaee-108">For more information about data entities, see [Data entities](../../dev-itpro/data-entities/data-entities.md).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="8aaee-109">استيراد ‏‏حركات بطاقات الائتمان</span><span class="sxs-lookup"><span data-stu-id="8aaee-109">Import credit card transactions</span></span>

1. <span data-ttu-id="8aaee-110">في صفحة **حركات بطاقات الائتمان‬**، حدد **استيراد الحركات**.</span><span class="sxs-lookup"><span data-stu-id="8aaee-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="8aaee-111">إذا كنت تفتح إدارة البيانات للمرة الأولى، فيجب على النظام تحديث قائمة كيانات البيانات قبل أن تتمكن من المتابعة.</span><span class="sxs-lookup"><span data-stu-id="8aaee-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="8aaee-112">في حقل **الاسم**، أدخل وصفًا فريدًا لوظيفة الاستيراد.</span><span class="sxs-lookup"><span data-stu-id="8aaee-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="8aaee-113">في حقل **تنسيق بيانات المصدر**، حدد تنسيق الملف الذي يحتوي على حركات بطاقات الائتمان لاستيرادها.</span><span class="sxs-lookup"><span data-stu-id="8aaee-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="8aaee-114">حدد **تحميل**، ثم ابحث عن الملف المطلوب استيراده وحدده.</span><span class="sxs-lookup"><span data-stu-id="8aaee-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="8aaee-115">بعد تحميل الملف، تحقق من تعيين ملف حركات بطاقات الائتمان وأعمدة كيان بيانات حركات بطاقات الائتمان عن طريق تحديد ارتباط **عرض التعيين‬** في الإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="8aaee-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="8aaee-116">إذا كان هناك أخطاء في التعيين، أو إذا تحتم تغيير التعيين، فأدخل تغييرات التعيين إما من علامة التبويب **مؤثرات عرض التعيين** أو علامة التبويب **تفاصيل‏‎ التعيين**.</span><span class="sxs-lookup"><span data-stu-id="8aaee-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="8aaee-117">لأتمتة حركات بطاقات الائتمان، حدد **إنشاء وظيفة بيانات متكررة‬**.</span><span class="sxs-lookup"><span data-stu-id="8aaee-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="8aaee-118">يمكنك بعد ذلك تعيين التكرار الذي يحدد عدد المرات التي يجب أن يتم فيها استيراد حركات بطاقات الائتمان.</span><span class="sxs-lookup"><span data-stu-id="8aaee-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="8aaee-119">عند الانتهاء، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8aaee-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="8aaee-120">لاستيراد الملف المحدد الآن، حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="8aaee-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="8aaee-121">في حالة حدوث أخطاء أثناء عملية الاستيراد، يمكنك عرض سجل التنفيذ أو بيانات التشغيل المرحلي‬ للتعرف على الأخطاء التي يجب إصلاحه للمساعدة في ضمان نجاح عملية الاستيراد.</span><span class="sxs-lookup"><span data-stu-id="8aaee-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="8aaee-122">إذا كان يجب أن استيراد أكثر من تنسيق ملف واحد أو، فيجب إنشاء مهام استيراد منفصلة لكل نوع تنسيق.</span><span class="sxs-lookup"><span data-stu-id="8aaee-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="8aaee-123">إعادة تعيين حركات بطاقات الائتمان الخاصة بالموظفين الذين تم إنهاء خدماتهم</span><span class="sxs-lookup"><span data-stu-id="8aaee-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="8aaee-124">بعد أن يتم إنهاء سجل موظف، يتم تعطيل حساب خدمات مجال Active Directory (أو AD DS) للموظف.</span><span class="sxs-lookup"><span data-stu-id="8aaee-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="8aaee-125">ومع ذلك، قد تكون هناك حركات بطاقات ائتمان نشطة التي يجب إدخالها في حساب المصروفات ودفعها كتعويض.</span><span class="sxs-lookup"><span data-stu-id="8aaee-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="8aaee-126">من صفحة **حركات بطاقات الائتمان**، يمكنك إعادة تعيين الموظف لأي حركة بطاقة ائتمان حيث تم إنهاء خدمات الموظف المرتبط.</span><span class="sxs-lookup"><span data-stu-id="8aaee-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="8aaee-127">حدد حركة بطاقة ائتمان واحدة أو أكثر، ثم انقر فوق **إعادة تعيين الحركات**.</span><span class="sxs-lookup"><span data-stu-id="8aaee-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="8aaee-128">يمكنك بعد ذلك تحديد موظف آخر لتعيين حركات بطاقات الائتمان له.</span><span class="sxs-lookup"><span data-stu-id="8aaee-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="8aaee-129">بعد إعادة تعيين حركات بطاقات الائتمان، يمكن تحديدها لتقرير المصروفات ودفعها من خلال العملية المنتظمة لتعويض تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="8aaee-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

