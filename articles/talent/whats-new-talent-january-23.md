---
title: ما الجديد أو المتغير في Dynamics 365 for Talent Core HR‏ (23 يناير 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f27698c257301f52e5c77eaa8a04ca13a0315825
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/19/2019
ms.locfileid: "859594"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-23-2019"></a><span data-ttu-id="fc201-103">ما الجديد أو المتغير في Dynamics 365 for Talent Core HR‏ (23 يناير 2019)</span><span class="sxs-lookup"><span data-stu-id="fc201-103">What's new or changed in Dynamics 365 for Talent Core HR (January 23, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fc201-104">**الإصدار 8.1.2121**</span><span class="sxs-lookup"><span data-stu-id="fc201-104">**Build 8.1.2121**</span></span>

<span data-ttu-id="fc201-105">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Core HR.</span><span class="sxs-lookup"><span data-stu-id="fc201-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="fc201-106">التغييرات</span><span class="sxs-lookup"><span data-stu-id="fc201-106">Changes</span></span>

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a><span data-ttu-id="fc201-107">عدم عمل استيراد التعويض الثابت للموظفين عند إنشاء سجلات تعويض ثابت جديدة</span><span class="sxs-lookup"><span data-stu-id="fc201-107">Import of employee fixed compensation not working when creating new fixed compensation records</span></span>
<span data-ttu-id="fc201-108">تم إدخال تغيير على كيان التعويض الثابت للموظفين لاسترداد مستوى التعويض عند الاستيراد.</span><span class="sxs-lookup"><span data-stu-id="fc201-108">A change has been made to the employee fixed compensation entity to retrieve the compensation level upon import.</span></span> <span data-ttu-id="fc201-109">قبل هذا الإصدار، كانت تظهر رسالة تشير إلى أن المستوى كان مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="fc201-109">Prior to this release, a message was displayed indicating that the level was required.</span></span>

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a><span data-ttu-id="fc201-110">إزالة حقل "الحد الأدنى للرصيد" من مربع حوار "طلب إجازة"</span><span class="sxs-lookup"><span data-stu-id="fc201-110">Remove the minimum balance field from the time off request dialog box</span></span>
<span data-ttu-id="fc201-111">تمت إزالة حقل **الحد الأدنى للرصيد** من مربع حوار **طلب إجازة**.</span><span class="sxs-lookup"><span data-stu-id="fc201-111">The **Minimum balance** field has been removed from the **Time off request** dialog box.</span></span> <span data-ttu-id="fc201-112">يؤثر هذا التغيير على كافة المناطق التي يمكن فيها طلب زمن توقف.</span><span class="sxs-lookup"><span data-stu-id="fc201-112">This change affects all areas where time off can be requested.</span></span>

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a><span data-ttu-id="fc201-113">ترقية البيانات لمستويات التعويض التي لا تحدّث في جميع السيناريوهات</span><span class="sxs-lookup"><span data-stu-id="fc201-113">Data upgrade for compensation levels not updating in all scenarios</span></span>
<span data-ttu-id="fc201-114">تم إدخال تغيير لتحديث مستوى التعويض في خطط التعويض الثابت.</span><span class="sxs-lookup"><span data-stu-id="fc201-114">A change has been made to update the compensation level on fixed compensation plans.</span></span> <span data-ttu-id="fc201-115">سيؤدي هذا التغيير إلى ملء مستوى التعويض على الخطط الثابتة للوظيفة المعينة للموظف.</span><span class="sxs-lookup"><span data-stu-id="fc201-115">This change will populate the compensation level on fixed plans for the job assigned to the employee.</span></span>

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a><span data-ttu-id="fc201-116">تتوفر معلومات المرتبات في صفحة "إدارة التغييرات" فقط عند تسجيل الدخول كمسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="fc201-116">Payroll information in the Manage changes page is only available when logged in as System Administrator</span></span>
<span data-ttu-id="fc201-117">هذا التغيير يسمح للموظفين الذي يؤدون دور مسؤول المرتبات بالوصول إلى معلومات حول المرتبات‬ في صفحة **تغييرات المخطط الزمني > إدارة التغييرات** للمنصب.</span><span class="sxs-lookup"><span data-stu-id="fc201-117">This change allows employees with the Payroll Administrator role access to the payroll information on the **Changes timeline > Manage changes** page for the position.</span></span>

### <a name="job-fields-default-to-positions"></a><span data-ttu-id="fc201-118">تعيين قيم حقول الوظائف إلى المناصب بشكل افتراضي</span><span class="sxs-lookup"><span data-stu-id="fc201-118">Job fields default to positions</span></span>
<span data-ttu-id="fc201-119">عند تغيير الوظيفة في أحد المناصب، يتم تعيين قيم حقول الوظائف إلى المنصب بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="fc201-119">When changing the job on a position, job fields will default to the position.</span></span> <span data-ttu-id="fc201-120">سوف تظهر رسالة تنبيه توفر خيارًا يسمح بقبول القيم الافتراضية أو الاحتفاظ بالقيم الموجودة الخاصة بهذه الحقول.</span><span class="sxs-lookup"><span data-stu-id="fc201-120">An alert message will appear giving an option to accept the default values or keep the existing values for those fields.</span></span>

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a><span data-ttu-id="fc201-121">عدم ظهور فترة وضع الاختبار والتقويم للموظفين الذين سيتم تعيينهم في المستقبلي.</span><span class="sxs-lookup"><span data-stu-id="fc201-121">Probation period and calendar are not displayed for future hired employees.</span></span>
<span data-ttu-id="fc201-122">مع هذا التغيير، تمت إضافة الحقلين **فترة الاختبار** و**التقويم** إلى صفحة **إدارة التغييرات** للسماح بإدخال البيانات للموظفين السابقين واللاحقين.</span><span class="sxs-lookup"><span data-stu-id="fc201-122">With this change, **Probation period** and **Calendar** fields have been added to the **Manage changes** page to allow for data entry for future and past employees.</span></span>

### <a name="platform-update-23"></a><span data-ttu-id="fc201-123">update 23 للنظام الأساسي</span><span class="sxs-lookup"><span data-stu-id="fc201-123">Platform update 23</span></span>
<span data-ttu-id="fc201-124">تم تضمين إصلاحات أخطاء ثانوية كجزء من Platform update 23.</span><span class="sxs-lookup"><span data-stu-id="fc201-124">Minor bug fixes have been included as part of Platform update 23.</span></span> <span data-ttu-id="fc201-125">للحصول على مزيد من المعلومات، راجع [ما الجديد أو المتغير في Dynamics 365 for Finance and Operations platform update 23 (يناير 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span><span class="sxs-lookup"><span data-stu-id="fc201-125">For more information, see [What's new or changed in Dynamics 365 for Finance and Operations platform update 23 (January 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span></span> 
