---
title: تكوين معلمات إدارة المزايا لكل شركة
description: قم بتكوين المعلمات لإدارة الميزات لكل شركة في Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 87d4f1e7580b333fd17d3b779aafa47c5baed424
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805648"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="37a6a-103">تكوين معلمات إدارة المزايا لكل شركة</span><span class="sxs-lookup"><span data-stu-id="37a6a-103">Configure Benefits management parameters per company</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="37a6a-104">بالنسبة لكل مؤسسة تقدم مزايا، يجب عليك تكوين الإعدادات لرسائل البريد الإلكتروني لتأكيد المزايا.</span><span class="sxs-lookup"><span data-stu-id="37a6a-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="37a6a-105">تكوين إعدادات البريد الإلكتروني للتأكيد</span><span class="sxs-lookup"><span data-stu-id="37a6a-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="37a6a-106">في مساحة عمل **إدارة الميزات**، ضمن **الإعداد**، حدد **معلمات الموارد البشرية**.</span><span class="sxs-lookup"><span data-stu-id="37a6a-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="37a6a-107">في علامة التبويب **إدارة المزايا**، حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="37a6a-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="37a6a-108">الحقل</span><span class="sxs-lookup"><span data-stu-id="37a6a-108">Field</span></span> | <span data-ttu-id="37a6a-109">الوصف</span><span class="sxs-lookup"><span data-stu-id="37a6a-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="37a6a-110">**إرسال بريد إلكتروني للتأكيد**</span><span class="sxs-lookup"><span data-stu-id="37a6a-110">**Send confirmation email**</span></span> | <span data-ttu-id="37a6a-111">عند تشغيل هذه الميزة، سيتم إرسال بريد إلكتروني للتأكيد إلى الموظفين عند تسجيل الخروج من تجربة تسجيل المزايا في الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="37a6a-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="37a6a-112">**قالب البريد الإلكتروني للتأكيد**</span><span class="sxs-lookup"><span data-stu-id="37a6a-112">**Confirmation email template**</span></span> | <span data-ttu-id="37a6a-113">حدد قالب البريد الإلكتروني للمؤسسة لاستخدامه عند إرسال تأكيد التسجيل.</span><span class="sxs-lookup"><span data-stu-id="37a6a-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="37a6a-114">إذا لم تحدد نموذجًا، فسيتم إرسال البريد الإلكتروني العام التالي:</span><span class="sxs-lookup"><span data-stu-id="37a6a-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="37a6a-115">%EmployeeFirstName%،</span><span class="sxs-lookup"><span data-stu-id="37a6a-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="37a6a-116">تهانينا!</span><span class="sxs-lookup"><span data-stu-id="37a6a-116">Congratulations!</span></span> <span data-ttu-id="37a6a-117">لقد أكملت بنجاح التسجيل في المزايا.</span><span class="sxs-lookup"><span data-stu-id="37a6a-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="37a6a-118">شكرًا لك،</span><span class="sxs-lookup"><span data-stu-id="37a6a-118">Thank you,</span></span><br><span data-ttu-id="37a6a-119">مزايا <Company/Org name>.</span><span class="sxs-lookup"><span data-stu-id="37a6a-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="37a6a-120">**عنوان مرسل البريد الإلكتروني الافتراضي**</span><span class="sxs-lookup"><span data-stu-id="37a6a-120">**Default email sender address**</span></span> | <span data-ttu-id="37a6a-121">عنوان البريد الإلكتروني المراد استخدامه عند إرسال رسالة التأكيد عبر البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="37a6a-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="37a6a-122">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="37a6a-122">Select **Save**.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]