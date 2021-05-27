---
title: لا يمكن تكوين مجموعة أمان لمنشئ موقع التجارة أثناء النشر الأولي
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور مجموعة أمان Microsoft Azure Active Directory (Azure AD) لمنشئ موقع التجارة كخيار عند إنشاء مكونات التجارة الإلكترونية في Microsoft Dynamics Lifecycle Services (LCS) أثناء النشر الأولي لمستأجر التجارة الإلكترونية الجديد.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d29e560d0f7b2bbc2415d7a0f6fe18f2ca17dc7c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020722"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a><span data-ttu-id="57df7-103">لا يمكن تكوين مجموعة أمان لمنشئ موقع التجارة أثناء النشر الأولي</span><span class="sxs-lookup"><span data-stu-id="57df7-103">Can't configure a security group for Commerce site builder during initial deployment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="57df7-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور مجموعة أمان Microsoft Azure Active Directory (Azure AD) لمنشئ موقع التجارة كخيار عند إنشاء مكونات التجارة الإلكترونية في Microsoft Dynamics Lifecycle Services (LCS) أثناء النشر الأولي لمستأجر التجارة الإلكترونية الجديد.</span><span class="sxs-lookup"><span data-stu-id="57df7-104">This topic provides troubleshooting guidance that can help when the Microsoft Azure Active Directory (Azure AD) security group for Commerce site builder doesn't appear as an option when you create e-commerce components in Microsoft Dynamics Lifecycle Services (LCS) during initial deployment of a new e-commerce tenant.</span></span>

## <a name="description"></a><span data-ttu-id="57df7-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="57df7-105">Description</span></span>

<span data-ttu-id="57df7-106">عند إنشاء مكونات التجارة الإلكترونية كجزء من عملية نشر مستأجر التجارة الإلكترونية الجديد التي تشتمل على مكون منشئ موقع التجارة، فإن مجموعة أمان Azure AD لا تظهر كخيار في مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="57df7-106">When you create the e-commerce components as part of the process of deploying a new e-commerce tenant that includes the Commerce site builder component, the Azure AD security group doesn't appear as an option in the dialog box.</span></span>

## <a name="resolution"></a><span data-ttu-id="57df7-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="57df7-107">Resolution</span></span>

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a><span data-ttu-id="57df7-108">توفير موقع التجارة الإلكترونية مع مستخدم في المستأجر الصحيح</span><span class="sxs-lookup"><span data-stu-id="57df7-108">Provision the e-commerce site with a user in the correct tenant</span></span>

1. <span data-ttu-id="57df7-109">انتقل إلى [مدخل Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="57df7-109">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="57df7-110">تحت المستأجر تم توفير مشروع LCS لموقع التجارة الإلكترونية له، اتبع الإرشادات الموجودة في [إنشاء مجموعة أساسية وأضف الأعضاء باستخدام Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="57df7-110">Under the tenant that the LCS project for your e-commerce site was provisioned for, follow the instructions in [Create a basic group and add members using Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span></span>
1. <span data-ttu-id="57df7-111">انتقل إلى [LCS](https://lcs.dynamics.com/)، وقم بتسجيل الدخول باستخدام حساب يشترك في نفس المستأجر مثل مجموع أمان Azure AD التي قمت بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="57df7-111">Go to [LCS](https://lcs.dynamics.com/), and sign in by using an account that shares the same tenant as the Azure AD security group that you just created.</span></span> <span data-ttu-id="57df7-112">يجب أن يكون للحساب حق الوصول لعرض مجموعة أمان Azure AD.</span><span class="sxs-lookup"><span data-stu-id="57df7-112">The account must have access to view the Azure AD security group.</span></span>
1. <span data-ttu-id="57df7-113">قم بإكمال خطوات الإعداد لتكوين موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57df7-113">Complete the setup steps to configure the e-commerce site.</span></span> <span data-ttu-id="57df7-114">عندما تقوم بتوفير مكونات التجارة الإلكترونية، يجب أن تظهر الآن مجموعة الأمان كخيار في مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="57df7-114">When you provision the e-commerce components, the security group should now appear as an option in the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="57df7-115">لضمان ملء الحقل في مربع الحوار بقائمة مجموعات الأمان، يجب عليك تحديد **إدخال** بعد إدخال اسم مجمةعة أمان Azure AD التي قمت بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="57df7-115">To ensure that the field in the dialog box is filled with the list of security groups, you must select **Enter** after you enter the name of the Azure AD security group that you created.</span></span> <span data-ttu-id="57df7-116">ستسرد نتائج البحث كافة مجموعات أمان Azure AD التي تبدأ بنص البحث، ويمكن للمستخدم الوصول إليها.</span><span class="sxs-lookup"><span data-stu-id="57df7-116">The search results will list all the Azure AD security groups that start with the search text, and that the user has access to.</span></span> <span data-ttu-id="57df7-117">يمكنك استخدام مصطلح بحث أقصر للسماح بنتائج بحث أوسع.</span><span class="sxs-lookup"><span data-stu-id="57df7-117">You can use a shorter search term to allow for broader search results.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="57df7-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="57df7-118">Additional resources</span></span>

[<span data-ttu-id="57df7-119">إنشاء مجموعة أساسية وإضافة الأعضاء باستخدام Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="57df7-119">Create a basic group and add members using Azure Active Directory</span></span>](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[<span data-ttu-id="57df7-120">نشر مستأجر تجارة إلكترونية جديد</span><span class="sxs-lookup"><span data-stu-id="57df7-120">Deploy a new e-commerce tenant</span></span>](../deploy-ecommerce-site.md)