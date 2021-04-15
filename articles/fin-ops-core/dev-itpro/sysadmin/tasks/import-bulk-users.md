---
title: استيراد المستخدمين من Azure Active Directory
description: يمكن لمسؤولي النظام استخدام هذا الإجراء لاستيراد مستخدمين محددين يدويًا أو استيراد عدد كبير من المستخدمين من Azure Active Directory.
author: peakerbl
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9f03ae7197790c1aac6ebf3cb94ff7963b1291e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745779"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="74127-103">استيراد المستخدمين من Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="74127-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="74127-104">تحديد استيراد المستخدمين‬</span><span class="sxs-lookup"><span data-stu-id="74127-104">Import select users</span></span>

<span data-ttu-id="74127-105">يمكن لمسؤولي النظام استخدام هذا الإجراء لاستيراد مستخدمين محددين من Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="74127-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="74127-106">سيتم استيراد المستخدم مع شركة الجلسة الحالية كشركة افتراضية.</span><span class="sxs-lookup"><span data-stu-id="74127-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="74127-107">قم بتغيير الشركة الحالية إن أمكن قبل استيراد المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="74127-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="74127-108">انتقل إلى **إدارة النظام > مستخدمين > مستخدم**.</span><span class="sxs-lookup"><span data-stu-id="74127-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="74127-109">انقر فوق **استيراد المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="74127-109">Click **Import users**.</span></span>
4. <span data-ttu-id="74127-110">حدد المستخدمين الذين يجب استيرادهم وحدد **استيراد المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="74127-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="74127-111">بعد اكتمال الاستيراد، سيُطلب منك تعيين الأدوار للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="74127-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="74127-112">استيراد المستخدمين بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="74127-112">Import users in bulk</span></span>

<span data-ttu-id="74127-113">يمكن استخدام هذا الإجراء من قبل مسؤولي النظام لاستيراد عدد كبير من المستخدمين من خدمة Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="74127-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="74127-114">لاحظ أنه لا يمكن تحديد المستخدمين عند استخدام خيار استيراد الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="74127-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="74127-115">تشغيل الاستيراد كوظيفة دُفعة</span><span class="sxs-lookup"><span data-stu-id="74127-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="74127-116">سيتم استيراد المستخدم مع شركة الجلسة الحالية كشركة افتراضية.</span><span class="sxs-lookup"><span data-stu-id="74127-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="74127-117">قم بتغيير الشركة الحالية إن أمكن قبل استيراد المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="74127-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="74127-118">انتقل إلى **إدارة النظام > مستخدمين > مستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="74127-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="74127-119">انقر فوق **استيراد دُفعة‬**.</span><span class="sxs-lookup"><span data-stu-id="74127-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="74127-120">وسّع القسم **تشغيل في الخلفية‬‬**.</span><span class="sxs-lookup"><span data-stu-id="74127-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="74127-121">حدد **نعم** في حقل **معالجة الدُفعات**.</span><span class="sxs-lookup"><span data-stu-id="74127-121">Select **Yes** in the **Batch processing** field.</span></span>
6. <span data-ttu-id="74127-122">في حقل **مجموعة الدُفعات**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="74127-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="74127-123">هذه خطوة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="74127-123">This is an optional step.</span></span>  
7. <span data-ttu-id="74127-124">حدد **نعم** في الحقل **خاص**.</span><span class="sxs-lookup"><span data-stu-id="74127-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="74127-125">هذه خطوة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="74127-125">This is an optional step.</span></span>  
8. <span data-ttu-id="74127-126">حدد **نعم** في حقل **وظيفة مهمة**.</span><span class="sxs-lookup"><span data-stu-id="74127-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="74127-127">هذه خطوة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="74127-127">This is an optional step.</span></span>  
9. <span data-ttu-id="74127-128">في الحقل **فئة المراقبة**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="74127-128">In the **Monitoring category** field, select an option.</span></span>
10. <span data-ttu-id="74127-129">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="74127-129">Click **OK**.</span></span>

<span data-ttu-id="74127-130">بعد اكتمال الاستيراد، سيُطلب منك تعيين الأدوار للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="74127-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="74127-131">التشغيل في بيئة وضع الحماية</span><span class="sxs-lookup"><span data-stu-id="74127-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="74127-132">حدد **استيراد الدُفعات**.</span><span class="sxs-lookup"><span data-stu-id="74127-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="74127-133">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="74127-133">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]