---
title: تكوينات طلب المورّد
description: يصف هذا الموضوع الحقول المطلوبة تعبئتها في طلب مورد جديد.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: d238e0dbb754e88dcffa171456aa0a2336238cab
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "332508"
---
# <a name="vendor-request-configurations"></a><span data-ttu-id="64c3f-103">تكوينات طلب المورّد</span><span class="sxs-lookup"><span data-stu-id="64c3f-103">Vendor request configurations</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="64c3f-104">لإكمال طلب مورد، يجب على جهة اتصال المورد إكمال معالج تسجيل المورد المتوقع.</span><span class="sxs-lookup"><span data-stu-id="64c3f-104">To complete a vendor request, a vendor contact person must complete the prospective vendor registration wizard.</span></span>

<span data-ttu-id="64c3f-105">في نموذج **‏‫تكوينات طلب المورّد‬**، يمكنك إنشاء ملفات تعريف تحدد الحقول المطلوبة والحقول المرئية في معالج تسجيل المورد المتوقع.</span><span class="sxs-lookup"><span data-stu-id="64c3f-105">In the **Vendor request configurations** form, you can create profiles that specify required fields and visible fields in the prospective vendor registration wizard.</span></span>

<span data-ttu-id="64c3f-106">سيتم بدء تشغيل معالج المورد بطلب مستخدم المورد المتوقع في البلد/المنطقة التي يقوم المورد بمباشرة أعماله فيها.</span><span class="sxs-lookup"><span data-stu-id="64c3f-106">The vendor registration wizard will start out by asking the prospective vendor user which country/region the vendor is doing business in.</span></span> <span data-ttu-id="64c3f-107">تحدد هذه المعلومات التكوين القابل للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="64c3f-107">This information determines the applicable configuration.</span></span> <span data-ttu-id="64c3f-108">إذا يتم تحديد أي تكوين محدد لبلد/منطقة، فسيتم استخدام تكوين افتراضي.</span><span class="sxs-lookup"><span data-stu-id="64c3f-108">If no specific configuration is defined for a country/region, a default configuration will be used.</span></span>

### <a name="set-up-a-vendor-request-configuration"></a><span data-ttu-id="64c3f-109">إعداد تكوين طلب المورّد</span><span class="sxs-lookup"><span data-stu-id="64c3f-109">Set up a vendor request configuration</span></span>

<span data-ttu-id="64c3f-110">بشكل افتراضي، يتوفر تكوين مورد في نموذج تكوينات طلب المورد.</span><span class="sxs-lookup"><span data-stu-id="64c3f-110">By default, there is a vendor configuration available in the Vendor request configurations form.</span></span>

<span data-ttu-id="64c3f-111">يتعذر تحديد البلد/المناطق للتكوين الافتراضي، وبالتالي لا يمكن تغيير قسم **البلاد/المناطق**.</span><span class="sxs-lookup"><span data-stu-id="64c3f-111">It is not possible to select country/regions for the default configuration, so the **Countries/regions** section cannot be changed.</span></span>

1. <span data-ttu-id="64c3f-112">انقر فوق **‬‏‫التدبير وتحديد الموارد‬‏‫** > **الإعداد** > **الموردون**، ثم انقر فوق **تكوينات طلب المورد**.</span><span class="sxs-lookup"><span data-stu-id="64c3f-112">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2. <span data-ttu-id="64c3f-113">انقر فوق علامة التبويب **الحقول** لتعيين حالة الحقول المسرودة.</span><span class="sxs-lookup"><span data-stu-id="64c3f-113">Click the **Fields** tab to set the status of the listed fields.</span></span>
3. <span data-ttu-id="64c3f-114">مخفي (غير مرئي)</span><span class="sxs-lookup"><span data-stu-id="64c3f-114">Hidden (Not visible)</span></span>
4. <span data-ttu-id="64c3f-115">معروض (مرئي لكن ليس إلزامياً)</span><span class="sxs-lookup"><span data-stu-id="64c3f-115">Displayed (Visible but not mandatory)</span></span>
5. <span data-ttu-id="64c3f-116">مطلوب (مرئي وإلزامي)</span><span class="sxs-lookup"><span data-stu-id="64c3f-116">Required (Visible and mandatory)</span></span>
6. <span data-ttu-id="64c3f-117">انقر فوق علامة التبويب **المحتوى** لتحديد إذا كان سيتم عرض النص في المعالج، وإذا كان سيقر مستخدم المورد المتوقع بالموافقة على هذا قبل الانتقال إلى الخطوة التالية في المعالج.</span><span class="sxs-lookup"><span data-stu-id="64c3f-117">Click the **Content** tab to specify if text is going to be shown on the wizard and if there should be an acknowledgement that the prospective vendor user must accept this before moving to the next step in the wizard.</span></span> <span data-ttu-id="64c3f-118">ستتم المطالبة بالإقرار بأي بنود وشروط يجب أن يقبلها المستخدم للمتابعة.</span><span class="sxs-lookup"><span data-stu-id="64c3f-118">The acknowledgement will be requested for any terms and conditions that the user must accept to continue.</span></span>

<span data-ttu-id="64c3f-119">يمكنك أيضا إدخال رسالة تأكيد ستظهر عند الانتهاء من المعالج، ويمكنك إضافة استبيان أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="64c3f-119">You can also enter a confirmation message that will be displayed when the wizard is finalized, and you can add one or more questionnaires.</span></span>

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a><span data-ttu-id="64c3f-120">إنشاء تكوين مورد لبلد/منطقة محددة</span><span class="sxs-lookup"><span data-stu-id="64c3f-120">Create a vendor configuration for a specific country/region</span></span>
1.  <span data-ttu-id="64c3f-121">انقر فوق **‬‏‫التدبير وتحديد الموارد‬‏‫** > **الإعداد** > **الموردون**، ثم انقر فوق **تكوينات طلب المورد**.</span><span class="sxs-lookup"><span data-stu-id="64c3f-121">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="64c3f-122">انقر فوق **جديد** لإنشاء تكوين جديد وقم بتوفير اسمًا للتكوين.</span><span class="sxs-lookup"><span data-stu-id="64c3f-122">Click **New** to create a new configuration, and provide a name for the configuration.</span></span>
3.  <span data-ttu-id="64c3f-123">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="64c3f-123">Click **Save**.</span></span>
4.  <span data-ttu-id="64c3f-124">افتح علامة التبويب **البلاد/المناطق** لتحديد البلد/المنطقة التي ستستخدم في التكوين.</span><span class="sxs-lookup"><span data-stu-id="64c3f-124">Open the **Country/regions** tab to select the country/region that the configuration should be used for.</span></span>
5.  <span data-ttu-id="64c3f-125">أكمل التكوين باتباع الإرشادات الخاصة بالتكوين الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="64c3f-125">Complete the configuration by following the guidelines for the default configuration.</span></span>

