---
title: تكوين معلمات إدارة المزايا لكل شركة
description: قم بتكوين المعلمات لإدارة الميزات لكل شركة في Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 2943d0095e4c9421725b90e579b7cbb841038ab7
ms.sourcegitcommit: fd097f6f76f0d8428038fa3655b3188bf093b517
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692735"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="3754c-103">تكوين معلمات إدارة المزايا لكل شركة</span><span class="sxs-lookup"><span data-stu-id="3754c-103">Configure Benefits management parameters per company</span></span>

<span data-ttu-id="3754c-104">بالنسبة لكل مؤسسة تقدم مزايا، يجب عليك تكوين الإعدادات لرسائل البريد الإلكتروني لتأكيد المزايا.</span><span class="sxs-lookup"><span data-stu-id="3754c-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="3754c-105">تكوين إعدادات البريد الإلكتروني للتأكيد</span><span class="sxs-lookup"><span data-stu-id="3754c-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="3754c-106">في مساحة عمل **إدارة الميزات**، ضمن **الإعداد**، حدد **معلمات الموارد البشرية**.</span><span class="sxs-lookup"><span data-stu-id="3754c-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="3754c-107">في علامة التبويب **إدارة المزايا**، حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="3754c-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="3754c-108">الحقل</span><span class="sxs-lookup"><span data-stu-id="3754c-108">Field</span></span> | <span data-ttu-id="3754c-109">الوصف</span><span class="sxs-lookup"><span data-stu-id="3754c-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3754c-110">**إرسال بريد إلكتروني للتأكيد**</span><span class="sxs-lookup"><span data-stu-id="3754c-110">**Send confirmation email**</span></span> | <span data-ttu-id="3754c-111">عند تشغيل هذه الميزة، سيتم إرسال بريد إلكتروني للتأكيد إلى الموظفين عند تسجيل الخروج من تجربة تسجيل المزايا في الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="3754c-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="3754c-112">**قالب البريد الإلكتروني للتأكيد**</span><span class="sxs-lookup"><span data-stu-id="3754c-112">**Confirmation email template**</span></span> | <span data-ttu-id="3754c-113">حدد قالب البريد الإلكتروني للمؤسسة لاستخدامه عند إرسال تأكيد التسجيل.</span><span class="sxs-lookup"><span data-stu-id="3754c-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="3754c-114">إذا لم تحدد نموذجًا، فسيتم إرسال البريد الإلكتروني العام التالي:</span><span class="sxs-lookup"><span data-stu-id="3754c-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="3754c-115">%EmployeeFirstName%،</span><span class="sxs-lookup"><span data-stu-id="3754c-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="3754c-116">تهانينا!</span><span class="sxs-lookup"><span data-stu-id="3754c-116">Congratulations!</span></span> <span data-ttu-id="3754c-117">لقد أكملت بنجاح التسجيل في المزايا.</span><span class="sxs-lookup"><span data-stu-id="3754c-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="3754c-118">شكرًا لك،</span><span class="sxs-lookup"><span data-stu-id="3754c-118">Thank you,</span></span><br><span data-ttu-id="3754c-119">مزايا <Company/Org name>.</span><span class="sxs-lookup"><span data-stu-id="3754c-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="3754c-120">**عنوان مرسل البريد الإلكتروني الافتراضي**</span><span class="sxs-lookup"><span data-stu-id="3754c-120">**Default email sender address**</span></span> | <span data-ttu-id="3754c-121">عنوان البريد الإلكتروني المراد استخدامه عند إرسال رسالة التأكيد عبر البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="3754c-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="3754c-122">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="3754c-122">Select **Save**.</span></span>