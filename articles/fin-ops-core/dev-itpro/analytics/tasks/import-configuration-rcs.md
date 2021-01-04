---
title: (التقارير الإلكترونية) استيراد التكوينات من RCS
description: يوفر هذا الموضوع معلومات حول كيفية قيام مستخدم باستيراد إصدار جديد من تكوين ER من RCS.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b591df3d384e8dc59646ebb9d0205001db040a55
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684177"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="e907b-103">(التقارير الإلكترونية) استيراد التكوينات من RCS</span><span class="sxs-lookup"><span data-stu-id="e907b-103">(ER) Import configurations from RCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e907b-104">تشرح الخطوات التالية كيف يمكن لمستخدم له دور مسؤول النظام أو مطور التقارير الإلكترونية استيراد إصدار جديد من تكوين التقارير الإلكترونية من Microsoft Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="e907b-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="e907b-105">في هذا المثال، ستقوم بتحديد إصدار تكوين التقارير الإلكترونية الذي تم تكوينه في مثيل RCS واستيراده إلى المثيل الحالي من للشركة النموذجية Litware, Inc. يمكن إجراء هذه الخطوات في أي شركة لأن تكوينات التقارير الإلكترونية مشتركة بين الشركات.</span><span class="sxs-lookup"><span data-stu-id="e907b-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="e907b-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الموضوع، [إنشاء موفرات تكوين وتحديدها بالحالة نشط](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e907b-106">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="e907b-107">لإكمال هذه الخطوات، يجب أيضا أن يكون لديك حق الوصول إلى مثيل RCS يحتوي على تكوين ER بالحالة إما **مكتمل** أو **مشترك**.</span><span class="sxs-lookup"><span data-stu-id="e907b-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="e907b-108">انتقل إلى **إدارة المؤسسة** > **مساحات العمل‬** > **إعداد التقارير الإلكترونية**‬.</span><span class="sxs-lookup"><span data-stu-id="e907b-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="e907b-109">تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كـ **نشط**.</span><span class="sxs-lookup"><span data-stu-id="e907b-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="e907b-110">في حالة عدم رؤية موفر التكوين هذا، أكمل الخطوات المذكورة في الموضوع [إنشاء موفرات تكوين وتحديدها بالحالة نشط‬](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e907b-110">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="e907b-111">في حالة عدم توفير بيئة RCS للشركة الخاصة بك، حدد الارتباط الخارجي **Regulatory services - التكوين** واتبع الإرشادات لتوفير بيئة RCS.</span><span class="sxs-lookup"><span data-stu-id="e907b-111">If you have no RCS environment provisioned to your company, select **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="e907b-112">حدد **معلمات التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="e907b-112">Select **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="e907b-113">حدد علامة التبويب **RCS**.</span><span class="sxs-lookup"><span data-stu-id="e907b-113">Select the **RCS** tab.</span></span> 
6. <span data-ttu-id="e907b-114">إذا تم بالفعل توفير بيئة RCS لشركك، فاستخدم المقدم منها على عناوين URL للصفحة للوصول إليها.</span><span class="sxs-lookup"><span data-stu-id="e907b-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="e907b-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e907b-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="e907b-116">تسجيل مستودع ER جديد.</span><span class="sxs-lookup"><span data-stu-id="e907b-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="e907b-117">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e907b-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="e907b-118">حدد الموفر Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="e907b-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="e907b-119">حدد المستودعات.</span><span class="sxs-lookup"><span data-stu-id="e907b-119">Select Repositories.</span></span> 
4. <span data-ttu-id="e907b-120">حدد إضافة لفتح مربع الحوار المنسدل.</span><span class="sxs-lookup"><span data-stu-id="e907b-120">Select Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="e907b-121">في الحقل "نوع مستودع التكوين"، أدخل "RCS".</span><span class="sxs-lookup"><span data-stu-id="e907b-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="e907b-122">حدد إنشاء مستودع.</span><span class="sxs-lookup"><span data-stu-id="e907b-122">Select Create repository.</span></span> 
7. <span data-ttu-id="e907b-123">في حقل اسم شاشة بيئة RCS، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e907b-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="e907b-124">حدد مثيل RCS المرغوب.</span><span class="sxs-lookup"><span data-stu-id="e907b-124">Select the desired RCS instance.</span></span> <span data-ttu-id="e907b-125">يمكن أن يكون لديك العديد منها.</span><span class="sxs-lookup"><span data-stu-id="e907b-125">You can have several of them.</span></span> 
9. <span data-ttu-id="e907b-126">حدد موافق.</span><span class="sxs-lookup"><span data-stu-id="e907b-126">Select OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="e907b-127">استيراد تكوينات التقارير الإلكترونية من مستودع مستند إلى RCS</span><span class="sxs-lookup"><span data-stu-id="e907b-127">Import ER configurations from RCS-based repository</span></span>
1. <span data-ttu-id="e907b-128">حدد **إظهار عوامل التصفية**.</span><span class="sxs-lookup"><span data-stu-id="e907b-128">Select **Show filters**.</span></span> 
2. <span data-ttu-id="e907b-129">أدخل قيمة عامل التصفية لـ "RCS" في حقل **الاسم** باستخدام مشغل عامل التصفية **يبدأ بـ**.</span><span class="sxs-lookup"><span data-stu-id="e907b-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="e907b-130">عند فتح المستودع المحدد، في الصفحة **الاتصال بـ Regulatory Configuration Services**، حدد ارتباط **انقر هنا للاتصال بـ Regulatory Configuration Services**.</span><span class="sxs-lookup"><span data-stu-id="e907b-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, select **Select here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="e907b-131">حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="e907b-131">Select **Open**.</span></span> 
5. <span data-ttu-id="e907b-132">حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="e907b-132">Select **Close**.</span></span> 
6. <span data-ttu-id="e907b-133">حدد الإصدار المطلوب من تكوين التقارير الإلكترونية، ثم حدد **استيراد** لإحضاره إلى المثيل الحالي.</span><span class="sxs-lookup"><span data-stu-id="e907b-133">Select the desired version of ER configuration and select **Import** to bring it in the current instance.</span></span>

