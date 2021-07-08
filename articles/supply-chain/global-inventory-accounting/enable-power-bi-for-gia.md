---
title: تمكين Power BI لمحاسبة المخزون العالمي
description: يصف هذا الموضوع كيفية تمكين Microsoft Power BI لمحاسبة المخزون العالمي.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273107"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a><span data-ttu-id="8fc1b-103">تمكين Power BI لمحاسبة المخزون العالمي</span><span class="sxs-lookup"><span data-stu-id="8fc1b-103">Enable Power BI for Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="8fc1b-104">يمكنك تثبيت الإطارات المتجانبة ولوحات المعلومات والتقارير من حساب [PowerBI.com](https://powerbi.com/) الخاص بك إلى مساحة عمل تطبيق Microsoft Dynamics 365 .</span><span class="sxs-lookup"><span data-stu-id="8fc1b-104">You can pin tiles, dashboards, and reports from your [PowerBI.com](https://powerbi.com/) account to your Microsoft Dynamics 365 application workspace.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8fc1b-105">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="8fc1b-105">Prerequisites</span></span>

<span data-ttu-id="8fc1b-106">يجب أن تكون المتطلبات الأساسية التالية في مكانها قبل تمكين تقارير Power BI:</span><span class="sxs-lookup"><span data-stu-id="8fc1b-106">The following prerequisites must be in place before you can enable Power BI reporting:</span></span>

- <span data-ttu-id="8fc1b-107">يجب أن تكون مسؤول نظام في تطبيق Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8fc1b-107">You must be a system administrator in the Dynamics 365 application.</span></span>
- <span data-ttu-id="8fc1b-108">يجب أن يكون لديك حساب [PowerBI.com](https://powerbi.com/).</span><span class="sxs-lookup"><span data-stu-id="8fc1b-108">You must have a [PowerBI.com](https://powerbi.com/) account.</span></span>
- <span data-ttu-id="8fc1b-109">يجب أن يكون لديك لوحة معلومات واحدة وتقرير واحد على الأقل في حساب Power BI الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="8fc1b-109">You must have at least one dashboard and one report in your Power BI account.</span></span>
- <span data-ttu-id="8fc1b-110">يجب أن تكون مسؤولاً عن حساب Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="8fc1b-110">You must be an administrator for your Azure Active Directory (Azure AD) account.</span></span>
- <span data-ttu-id="8fc1b-111">يجب أن يكون المجال Azure AD هو نفس المجال الذي استخدمته لحساب [PowerBI.com](https://powerbi.com/).</span><span class="sxs-lookup"><span data-stu-id="8fc1b-111">The Azure AD domain must be the same domain that you used for your [PowerBI.com](https://powerbi.com/) account.</span></span>

## <a name="setup"></a><span data-ttu-id="8fc1b-112">الإعداد</span><span class="sxs-lookup"><span data-stu-id="8fc1b-112">Setup</span></span>

<span data-ttu-id="8fc1b-113">اتبع الخطوات التالية لإعداد تكامل Power BI.</span><span class="sxs-lookup"><span data-stu-id="8fc1b-113">To set up the Power BI integration, follow these steps.</span></span>

1. <span data-ttu-id="8fc1b-114">سجل دخولك إلى [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="8fc1b-114">Sign in to [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="8fc1b-115">انتقل إلى **مكتبة الأصول المشتركة**، حدد نموذج التقرير **Power BI**، كنوع الأصل، وقم بتنزيل الحزمة **محاسبة المخزون العالمي**.</span><span class="sxs-lookup"><span data-stu-id="8fc1b-115">Go to **Shared asset library**, select **Power BI report model** as the asset type, and download the **Global Inventory Accounting** package.</span></span> 
1. <span data-ttu-id="8fc1b-116">قم بتسجيل الدخول إلى [PowerBI.com](https://app.powerbi.com/)، وقم بتحميل ملف تقرير **محاسبة المخزون العالمي** Power BI باتباع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="8fc1b-116">Sign in to [PowerBI.com](https://app.powerbi.com/), and upload the **Global Inventory Accounting** Power BI report file by following these steps:</span></span>

    1. <span data-ttu-id="8fc1b-117">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8fc1b-117">Select **New**.</span></span>
    1. <span data-ttu-id="8fc1b-118">حدد **تحميل ملف**.</span><span class="sxs-lookup"><span data-stu-id="8fc1b-118">Select **Upload a file**.</span></span>
    1. <span data-ttu-id="8fc1b-119">حدد ملف التقرير **محاسبة المخزون العالمي** Power BI.</span><span class="sxs-lookup"><span data-stu-id="8fc1b-119">Select the **Global Inventory Accounting** Power BI report file.</span></span>

1. <span data-ttu-id="8fc1b-120">قم بتكوين التقرير **محاسبة المخزون العالمي** Power BI باتباع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="8fc1b-120">Configure the **Global Inventory Accounting** Power BI report by following these steps:</span></span>

    1. <span data-ttu-id="8fc1b-121">انتقل إلى **مساحة العمل الخاصة بي**، وابحث عن مجموعة البيانات الخاصة بمحاسبة المخزون العالمي، ثم في القائمة **الخيارات**، حدد **الإعدادات**.</span><span class="sxs-lookup"><span data-stu-id="8fc1b-121">Go to **My workspace**, find the dataset for Global Inventory Accounting, and then, on the **Options** menu, select **Settings**.</span></span>
    1. <span data-ttu-id="8fc1b-122">في **إعدادات محاسبة المخزون العالمي**، قم بتوسيع **المعلمات**، وقم بتحديث كل المعلمات كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="8fc1b-122">In **Settings for Global inventory accounting**, expand **Parameters**, and update all parameters as required.</span></span>

1. <span data-ttu-id="8fc1b-123">قم بتسجيل التطبيق كما هو موضح في [تكوين تكامل PowerBI.com](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span><span class="sxs-lookup"><span data-stu-id="8fc1b-123">Register the application as described in [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span></span>
1. <span data-ttu-id="8fc1b-124">قم بتكامل ملف التقرير **محاسبة المخزون العالمي** Power BI في Dynamics 365 Supply Chain Management باتباع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="8fc1b-124">Integrate the **Global Inventory Accounting** Power BI report file into Dynamics 365 Supply Chain Management by following these steps:</span></span>

    1. <span data-ttu-id="8fc1b-125">انتقل إلى **إدارة النظام \> الإعداد \> تكوين PowerBI.com**.</span><span class="sxs-lookup"><span data-stu-id="8fc1b-125">Go to **System administration \> Setup \> PowerBI.com configuration**.</span></span>
    1. <span data-ttu-id="8fc1b-126">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="8fc1b-126">Select **Edit**.</span></span>
    1. <span data-ttu-id="8fc1b-127">حدد **تمكين تكامل PowerBI.Com**.</span><span class="sxs-lookup"><span data-stu-id="8fc1b-127">Select **Enable PowerBI.Com integration**.</span></span>
    1. <span data-ttu-id="8fc1b-128">في الحقل **معرف التطبيق**، أدخل معرف التطبيق:</span><span class="sxs-lookup"><span data-stu-id="8fc1b-128">In the **Application ID** field, enter the application ID.</span></span>
    1. <span data-ttu-id="8fc1b-129">في الحقل **مفتاح التطبيق**، أدخل مفتاح التطبيق:</span><span class="sxs-lookup"><span data-stu-id="8fc1b-129">In the **Application key** field, enter the application key.</span></span>
    1. <span data-ttu-id="8fc1b-130">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8fc1b-130">Select **Save**.</span></span>

1. <span data-ttu-id="8fc1b-131">قم بتحديث الصفحة بحيث يظهر مربع حوار تسجيل دخول Power BI.</span><span class="sxs-lookup"><span data-stu-id="8fc1b-131">Refresh the page so that the Power BI sign-in dialog box appears.</span></span>
1. <span data-ttu-id="8fc1b-132">في علامة التبويب **الخيارات**، حدد **فتح كتالوج التقارير**، ثم حدد ملف التقرير **محاسبة المخزون العالمي** Power BI الذي قمت بتحميله مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="8fc1b-132">On the **Options** tab, select **Open report catalog**, and then select the **Global Inventory Accounting** Power BI report file that you uploaded earlier.</span></span>
1. <span data-ttu-id="8fc1b-133">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8fc1b-133">Refresh the page.</span></span> <span data-ttu-id="8fc1b-134">يجب أن ترى أنه تمت إضافة التقرير الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="8fc1b-134">You should see that your report has been added.</span></span>
1. <span data-ttu-id="8fc1b-135">ضمن تقارير **Power BI**، حدد الارتباط **محاسبة المخزون العالمي**.</span><span class="sxs-lookup"><span data-stu-id="8fc1b-135">Under **Power BI reports**, select the **Global Inventory Accounting** link.</span></span>

<span data-ttu-id="8fc1b-136">للحصول على مزيد من المعلومات، راجع [تكوين تكامل PowerBI.com](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span><span class="sxs-lookup"><span data-stu-id="8fc1b-136">For more information, see [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span></span>
